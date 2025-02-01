import greenfoot.*;

public class Greep extends Actor {
    public void act() {
        followPheromones();
        move(1); // Двигаться вперед
    }

    private void followPheromones() {
        // Найти все феромоны в радиусе 100 пикселей
        java.util.List<Pheromone> pheromones = getObjectsInRange(100, Pheromone.class);

        if (!pheromones.isEmpty()) {
            // Найти феромон с наибольшей интенсивностью
            Pheromone strongestPheromone = null;
            for (Pheromone p : pheromones) {
                if (strongestPheromone == null || p.getIntensity() > strongestPheromone.getIntensity()) {
                    strongestPheromone = p;
                }
            }

            // Повернуться в сторону феромона
            if (strongestPheromone != null) {
                turnTowards(strongestPheromone.getX(), strongestPheromone.getY());
            }
        }
    }
}
