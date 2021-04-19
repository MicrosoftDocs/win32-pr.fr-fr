---
description: La valeur de la propriété Résumé de l’objet transmet le nom du produit, de la transformation ou du correctif logiciel qui est installé par le package.
ms.assetid: fb08a240-db30-477f-8dc0-701156d73cfc
title: Propriété de résumé de l’objet
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d21139f686bc8a6cfc5ba2edecdfc57c349d84ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535958"
---
# <a name="subject-summary-property"></a>Propriété de résumé de l’objet

La valeur de la propriété Résumé de l' **objet** transmet le nom du produit, de la transformation ou du correctif logiciel qui est installé par le package.

C’est à l’auteur d’une base de données d’installation, d’une transformation ou d’un package de correctifs de fournir la valeur de cette propriété dans les informations de résumé. Les auteurs doivent effectuer les opérations suivantes pour déterminer la valeur correcte.

-   Définissez la propriété Résumé de l' **objet** d’un package d’installation sur la même valeur que la propriété [**ProductName**](productname.md) .
-   Définissez la propriété Résumé de l' **objet** dans une transformation sur la même valeur que la propriété Résumé de l' **objet** dans le package d’installation d’origine.
-   Définissez la propriété Résumé de l' **objet** dans les informations récapitulatives d’un package de correctifs sur une brève description du correctif qui comprend le nom du produit.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**PATCHNEWSUMMARYSUBJECT**](patchnewsummarysubject.md)
</dt> <dt>

[Descriptions des propriétés de synthèse](summary-property-descriptions.md)
</dt> </dl>

 

 




