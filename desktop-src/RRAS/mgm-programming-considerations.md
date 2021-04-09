---
title: Considérations sur la programmation de MGM
description: Lorsque vous développez des clients du gestionnaire de groupe de multidiffusion, observez les instructions suivantes
ms.assetid: 48451a76-81e0-4d60-acb3-c9ec55de32b4
keywords:
- Multidiffusion, considérations de programmation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e442de1dcb2da5a8664648587a88f05feaee970
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840389"
---
# <a name="mgm-programming-considerations"></a>Considérations sur la programmation de MGM

Lorsque vous développez des clients du gestionnaire de groupe de multidiffusion, observez les instructions suivantes :

-   Les appels de fonction doivent être effectués à partir du processus de routeur. Si les fonctions sont appelées à partir d’un autre processus, leurs résultats ne seront pas valides ; le client n’interagit pas avec le gestionnaire de groupe de multidiffusion.
-   Les clients qui utilisent l’API MGM doivent fournir leur propre vérification des erreurs, garantissant que seules les données valides sont transmises au gestionnaire de groupe de multidiffusion. Les fonctions MGM ne retournent pas de messages d’erreur détaillés sur les paramètres non valides ; la \_ valeur du paramètre non valide de l’erreur \_ est retournée sans explication.
-   Les clients doivent faire preuve de prudence lors de l’utilisation de verrous lors de l’appel de fonctions MGM. Cela peut empêcher les blocages. Lors de l’appel de fonctions MGM, les clients ne doivent pas contenir de verrous qui peuvent être maintenus simultanément dans un rappel du gestionnaire de groupe de multidiffusion.

 

 




