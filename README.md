maturin-docker
==

### **Image to publish and build with pyo3-pack with CI services like gitlab, multiple versions of python supported with tags.**

## Exemple gitlab-ci.yml

```
image: samblaise/pyo3-pack:3.6

stages:
  - build
  - publish
 
build:
  stage: build
  script:
    - pyo3-pack build
    
publish:
  stage: publish
  script:
    - maturin publish -u user -p $password
```



