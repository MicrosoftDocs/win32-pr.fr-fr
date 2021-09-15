---
description: L’action ProcessComponents inscrit et désinscrit les composants, leurs chemins d’accès aux clés et les clients des composants.
ms.assetid: 8ad418c0-9bba-41d0-a96c-2c7b1c2467d9
title: Action ProcessComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aef1f71e9a50b714a12848fc9f923d1866c2e40
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413945"
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



 

 

 



