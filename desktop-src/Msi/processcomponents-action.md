---
description: L’action ProcessComponents inscrit et désinscrit les composants, leurs chemins d’accès aux clés et les clients des composants.
ms.assetid: 8ad418c0-9bba-41d0-a96c-2c7b1c2467d9
title: Action ProcessComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1e866c6003052922dfc0e1fca5bd4ff8ea63d207eeb03c5ada22cf5f2d3e7b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119259279"
---
# <a name="processcomponents-action"></a>Action ProcessComponents

L’action ProcessComponents inscrit et désinscrit les composants, leurs chemins d’accès aux clés et les clients des composants. L’action ProcessComponents interroge la colonne keyPath de la [table Component](component-table.md) pour déterminer les chemins d’accès de keyPath. Cette inscription est utilisée par [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) pour retourner le chemin d’accès d’un composant pour un client produit.

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action ProcessComponents doit venir après l’action [InstallInitialize](installinitialize-action.md) .

## <a name="actiondata-messages"></a>Messages ActionData

Pour chaque composant en cours d’inscription.



| Champ | Description des données d’action      |
|-------|---------------------------------|
| \[1\] | ProductId                       |
| \[2\] | ComponentId                     |
| \[3\] | Chemin d’accès de la clé du composant. |



 

Pour chaque composant en cours d’annulation d’inscription.



| Champ | Description des données d’action |
|-------|----------------------------|
| \[1\] | ProductId                  |
| \[2\] | ComponentId                |



 

 

 



