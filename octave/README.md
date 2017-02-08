# Octave docker

## This docker has been created specifically to run Coursera  Standford Machine Learning course.



  >* [Standford Machine Learning course][77c4e76a]

  [77c4e76a]: https://www.coursera.org/learn/machine-learning/ "Course Machine Learning course"


## Running the container


  >* Command :
   <pre><code>docker run -it --rm  --user=$(id -u) \
       --env="DISPLAY" \
       --volume="/etc/group:/etc/group:ro" \
       --volume="/etc/shadow:/etc/shadow:ro" \
       --volume="/etc/sudoers.d:/etc/sudoers.d:ro" \
       --volume="/tmp/.X11-unix:/tmp/.X11-unix:rw" \
       --volume="$(pwd):/projects" \
   fara3/octave</code></pre>

  >* **The volumes above defined, allow to run "plot" charts from octave shell**
