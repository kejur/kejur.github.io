---
title: MySQL 事务的传播性
date: 2020-10-22 00:50
tags: MySQL
---


## 谁提出事务的传播性这个概念的呢？

是的，就是spring提出的

---
## 为什么提出呢？

解决事务嵌套的问题

---
## 什么是事务嵌套？


---
## 事务传播性的分类
- PROPAGATION_REQUIRED
        spring 默认的事务传播机制。
        外有则合，外无则开

- PROPAGATION_REQUIRES_NEW
        外挂自开

- PROPAGATION_SUPPORTS
        随外

- PROPAGATION_NOT_SUPPORTED
        外挂自不开

- PROPAGATION_NEVER
        外有则抛，自不开

- PROPAGATION_MANDATORY
        外无则抛

- PROPAGATION_NESTED
        回滚灵活

---
