---
description: Le Service VSS (VSS) fournit l’infrastructure système permettant d’exécuter des applications VSS sur des systèmes Windows.
ms.assetid: 237b2729-1e9b-4d0e-9c59-990e047a0360
title: Service VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 274e1e561b702dc2e69782fa5e9c2b47e6ea6a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751604"
---
# <a name="the-volume-shadow-copy-service"></a>Service VSS

Le Service VSS (VSS) fournit l’infrastructure système permettant d’exécuter des applications VSS sur des systèmes Windows.

Bien qu’il soit largement transparent pour l’utilisateur et le développeur, VSS effectue les opérations suivantes :

-   Coordonne les activités des fournisseurs, des enregistreurs et des demandeurs lors de la création et de l’utilisation des clichés instantanés
-   Fournit le fournisseur système par défaut
-   Implémente la fonctionnalité de pilote de bas niveau nécessaire pour que tout fournisseur fonctionne

Le service VSS démarre à la demande ; il doit donc être activé pour les opérations VSS puissent être effectuées.

 

 



