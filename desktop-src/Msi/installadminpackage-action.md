---
description: L’action InstallAdminPackage copie la base de données du produit sur le point d’installation d’administration, qui est défini par la propriété TARGETDIR.
ms.assetid: 9781f14b-0264-4d00-9a83-bd5400c614ec
title: Action InstallAdminPackage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1879d711e1a52a7121326ba170bb3a004fbfb4ee988b35d19a16e1a53c3e2811
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996589"
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



 

## <a name="remarks"></a>Remarques

L’action InstallAdminPackage met également à jour les informations récapitulatives de la base de données et supprime tous les fichiers CAB situés dans les flux de données une fois la base de données copiée.

 

 



