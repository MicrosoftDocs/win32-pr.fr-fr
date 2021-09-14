---
description: La propriété Résumé du nombre de pages contient la version minimale du programme d’installation requise par le package d’installation.
ms.assetid: ee3aaeed-166c-4591-ae3e-642c1204a5ca
title: Propriété du résumé du nombre de pages
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ec5e319450bb7a7db5515587be7777ad3e657d3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127218801"
---
# <a name="page-count-summary-property"></a>Propriété du résumé du nombre de pages

La propriété **Résumé du nombre de pages** contient la version minimale du programme d’installation requise par le package d’installation. pour un minimum de Windows Installer 2,0, cette propriété doit être définie sur l’entier 200. pour un minimum de Windows Installer 3,0, cette propriété doit être définie sur l’entier 300. pour un minimum de Windows Installer 3,1, cette propriété doit être définie sur 301. pour un minimum de Windows Installer 4,5, cette propriété doit être définie sur 405. pour un minimum de Windows Installer 5,0, cette propriété doit être définie sur 500.

pour les [Packages Windows Installers 64 bits](64-bit-windows-installer-packages.md), cette propriété doit être définie sur l’entier 200 ou supérieur. pour les Packages de Windows Installer 64 bits sur la plateforme Arm64, cette propriété doit être définie sur l’entier 500 ou supérieur.

Pour un package de transformation, la propriété **Résumé du nombre de pages** contient la version minimale du programme d’installation requise pour traiter la transformation. Défini sur la plus grande des deux valeurs de propriété **récapitulatives du nombre de pages** qui appartiennent aux bases de données utilisées pour générer la transformation.

Pour un package de correctifs, la propriété de **Résumé du nombre de pages** est définie sur null.

Cette propriété de résumé est obligatoire.

cette propriété peut être utilisée pour créer un package qui ne peut être installé que par la version minimale ou ultérieure spécifiée du Windows Installer.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Descriptions des propriétés de synthèse](summary-property-descriptions.md)
</dt> </dl>

 

 




