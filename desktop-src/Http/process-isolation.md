---
title: Isolement des processus
description: L’API du serveur HTTP version 2,0 offre la possibilité de créer un service plus sûr et plus fiable en isolant les processus de travail qui traitent les demandes sur la file d’attente des demandes.
ms.assetid: 893741b7-025c-4642-aff4-a5d69244763f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efcfccc78bbef435aa0c74e918003383135bc4ed
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2021
ms.locfileid: "103869345"
---
# <a name="process-isolation"></a>Isolement des processus

L’API du serveur HTTP version 2,0 offre la possibilité de créer un service plus sûr et plus fiable en isolant les processus de travail qui traitent les demandes sur la file d’attente des demandes. La file d’attente des demandes est créée et administrée par un contrôleur ou un processus de création qui contrôle strictement l’accès à celle-ci. Le processus de contrôleur lance un ou plusieurs processus de travail distincts qui effectuent des e/s sur la file d’attente des demandes. Le processus du contrôleur s’exécute avec des privilèges d’administration et configure la file d’attente des demandes, tandis que le travail de moindre privilège traite les demandes d’accès et de service à partir de la file d’attente des demandes. Cette architecture prend en charge la stratégie des applications qui s’exécutent sous le « moindre privilège » et réduit le risque de failles de sécurité introduites par du code tiers qui peut s’exécuter dans les processus de travail.

L’accès à la file d’attente des demandes est accordé lorsque le processus du contrôleur crée la file d’attente des demandes avec un nom et une liste de Access Control (ACL). Les applications Web incluses dans la liste de contrôle d’accès peuvent ouvrir une file d’attente de demandes existante par nom. Le processus de création peut également être un processus de travail dans la file d’attente des demandes. Pour plus d’informations, consultez la rubrique [file d’attente des demandes nommées](named-request-queue.md) . Le diagramme suivant illustre l’architecture d’une application HTTP standard exécutée avec le modèle de processus de travail :

![Diagramme qui montre l’architecture d’une application H T T P à l’aide du modèle de processus de travail.](images/processisolation.png)

Les processus de travail individuels au sein de l’application sont isolés des autres processus de travail, et l’intégrité de chaque processus de travail peut être surveillée par le processus du contrôleur. Le processus du contrôleur est isolé des processus de travail. Les composants de l’architecture HTTP sont décrits ci-dessous :

-   Processus du créateur ou du contrôleur : le processus du contrôleur peut s’exécuter avec ou sans privilèges d’administrateur pour surveiller l’intégrité et configurer le service. En général, le processus de contrôleur crée une session serveur unique pour le service et définit les groupes d’URL sous la session serveur. Le groupe d’URL auquel une URL particulière est associée détermine la file d’attente de demandes qui sert d’espace de noms à l’espace de noms indiqué par l’URL spécifique. Le processus de contrôleur crée également la file d’attente des demandes et lance les processus de travail qui peuvent accéder à la file d’attente des demandes.
-   Processus de travail : les processus de travail, lancés par le processus de contrôleur, effectuent des e/s sur la file d’attente de demandes qui est associée aux URL qu’ils service. L’application Web est autorisée à accéder à la file d’attente des demandes par le processus du contrôleur dans la liste de contrôle d’accès lorsque la file d’attente des demandes est créée. À moins que l’application Web soit également le processus de création, elle ne gère pas le service ou ne configure pas la file d’attente des demandes. Le processus de contrôleur communique le nom de la file d’attente des demandes au processus de travail et le processus de travail ouvre la file d’attente des demandes par nom. Les processus de travail peuvent charger des applications Web tierces sans introduire de failles de sécurité dans d’autres parties de l’application.
-   File d’attente de demandes : la file d’attente des demandes est créée et configurée par le processus du contrôleur. Le contrôleur spécifie les processus qui sont autorisés à accéder à la file d’attente des demandes dans la liste de contrôle d’accès lorsque la file d’attente des demandes est créée.
-   Session serveur : le processus de contrôleur crée et configure généralement une session serveur unique pour l’application. La session serveur gère les propriétés de configuration de l’application entière. Les groupes d’URL sont créés sous la session serveur par le processus du contrôleur.
-   Groupe d’URL : le processus de contrôleur crée les groupes d’URL sous la session du serveur et configure le groupe d’URL indépendamment de la session du serveur. Les URL sont ajoutées au groupe par le processus du contrôleur. Les demandes sont routées vers la file d’attente de demandes à laquelle le groupe d’URL est associé.

 

 




