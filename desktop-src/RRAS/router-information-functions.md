---
title: Fonctions d’informations de routeur
description: Utilisez les fonctions suivantes pour manipuler les en-têtes et les blocs d’informations de routeur. Un en-tête d’information est composé de métadonnées privées et de blocs d’informations. Les blocs d’informations sont des tableaux de structures d’informations de différents types.
ms.assetid: e88720aa-080b-4d87-a442-1b436c256ca6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f694d2dcd140d8af8950fa7a2a4ae5049a679ff8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127239519"
---
# <a name="router-information-functions"></a>Fonctions d’informations de routeur

Utilisez les fonctions suivantes pour manipuler les en-têtes et les blocs d’informations de routeur. Un en-tête d’information est composé de métadonnées privées et de blocs d’informations. Les blocs d’informations sont des tableaux de [structures d’informations](router-information-structures.md) de différents [types](router-information-enumerations.md).

Les fonctions suivantes permettent de manipuler les en-têtes d’informations :

-   [**MprInfoCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfocreate)
-   [**MprInfoDelete**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfodelete)
-   [**MprInfoDuplicate**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoduplicate)
-   [**MprInfoRemoveAll**](/windows/desktop/api/Mprapi/nf-mprapi-mprinforemoveall)

Les fonctions suivantes manipulent des blocs d’informations dans un en-tête d’information :

-   [**MprInfoBlockAdd**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockadd)
-   [**MprInfoBlockFind**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockfind)
-   [**MprInfoBlockQuerySize**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockquerysize)
-   [**MprInfoBlockRemove**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockremove)
-   [**MprInfoBlockSet**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockset)

La plupart des [fonctions d’administration et de configuration de routeur](understanding-mprinfo-functions-and-information-headers.md) utilisent des en-têtes d’informations.

 

 




