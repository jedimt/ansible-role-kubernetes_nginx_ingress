Ansible Role: Kubernetes nginx ingress
=========

Install the NGINX ingress controller for Kubernetes.

Requirements
------------

None

Role Variables
--------------

Specify the namespace to install the ingress controller:

    kube_namespace: monitoring

Dependencies
------------

None.

Example Playbook
----------------

    # ===========================================================================
    # Install Nginx ingress controller
    # ===========================================================================
    - name: Install nginx ingress controller
    hosts: k8s_master
    become: true
    gather_facts: false
    tags: play_nginx

    roles:
        - { role: ansible-role-kubernetes-nginx-ingress, kube_namespace: monitoring }

License
-------

MIT

Author Information
------------------

Aaron Patten
aaronpatten@gmail.com
