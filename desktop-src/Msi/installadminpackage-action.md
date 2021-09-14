---
description: L’action InstallAdminPackage copie la base de données du produit sur le point d’installation d’administration, qui est défini par la propriété TARGETDIR.
ms.assetid: 9781f14b-0264-4d00-9a83-bd5400c614ec
title: Action InstallAdminPackage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1eb2f86390fe3a47a6d100a887d34798e7f4d4c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121761"
---
# <a name="installadminpackage-action"></a>Action InstallAdminPackage

L’action InstallAdminPackage copie la base de données du produit sur le point d’installation d’administration, qui est défini par la propriété [**targetDir**](targetdir.md) .

## <a name="sequence-restrictions"></a>Restrictions de séquence

Il n’existe aucune restriction de séquence.

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action                                 |
|-------|------------------------------------------------------------|
| \[1\] | Nom des fichiers d’installation.                                     |
| \[6\] | Taille de la base de données.                                          |
| \[9\] | Identificateur de l’installation administrative – répertoire du point. |



 

## <a name="remarks"></a>Notes

L’action InstallAdminPackage met également à jour les informations récapitulatives de la base de données et supprime tous les fichiers CAB situés dans les flux de données une fois la base de données copiée.

 

 



