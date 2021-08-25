---
description: le Service VSS (VSS) fournit l’infrastructure système permettant d’exécuter des applications VSS sur des systèmes basés sur Windows.
ms.assetid: 237b2729-1e9b-4d0e-9c59-990e047a0360
title: Service VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f71e21ba0f20eaa0f3723cd0da6cb3efb89bae027678d154ab8b5b5568532ac8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866239"
---
# <a name="the-volume-shadow-copy-service"></a>Service VSS

le Service VSS (VSS) fournit l’infrastructure système permettant d’exécuter des applications VSS sur des systèmes basés sur Windows.

Bien qu’il soit largement transparent pour l’utilisateur et le développeur, VSS effectue les opérations suivantes :

-   Coordonne les activités des fournisseurs, des enregistreurs et des demandeurs lors de la création et de l’utilisation des clichés instantanés
-   Fournit le fournisseur système par défaut
-   Implémente la fonctionnalité de pilote de bas niveau nécessaire pour que tout fournisseur fonctionne

Le service VSS démarre à la demande ; il doit donc être activé pour les opérations VSS puissent être effectuées.

 

 



