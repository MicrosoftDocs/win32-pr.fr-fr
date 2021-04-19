---
description: Dans les informations de résumé d’un package d’installation, la propriété Résumé du nombre de mots indique le type d’image du fichier source.
ms.assetid: 1eeece25-4f24-4efe-879d-66ebbb6a9391
title: Propriété de résumé du nombre de mots
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c4200cb946f6948770d0c900c2df651b8fbff11
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532655"
---
# <a name="word-count-summary-property"></a>Propriété de résumé du nombre de mots

Dans les informations de résumé d’un package d’installation, la propriété **Résumé du nombre de mots** indique le type d’image du fichier source. Si cette propriété n’est pas présente, la valeur par défaut est zéro (0).

Cette propriété est un champ de bits. De nouveaux bits peuvent être ajoutés à l’avenir. À l’heure actuelle, les bits suivants sont disponibles.



| bit   | Valeur          | Description                                                                                                                                                                                                                                      |
|-------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bit 0 | 0 1<br/> | Noms de fichiers longs. Noms de fichiers courts.<br/>                                                                                                                                                                                                    |
| Bit 1 | 0 2<br/> | La source n’est pas compressée. La source est compressée.<br/>                                                                                                                                                                                         |
| Bit 2 | 0 4<br/> | La source est un support d’origine. La source est une image administrative créée par une installation administrative.<br/>                                                                                                                                 |
| Bit 3 | 0 8<br/> | Des privilèges élevés peuvent être nécessaires pour installer ce package. Des privilèges élevés ne sont pas nécessaires pour installer ce package.<br/> Disponible à partir de Windows Installer version 4,0 et Windows Vista ou Windows Server 2008.<br/> |



 

Celles-ci sont combinées pour attribuer à la propriété **Résumé du nombre de mots** une des valeurs suivantes qui indiquent un type d’image de fichier source.



| Valeur | Type                                                                                                                                                                                                                                                                                            |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Source d’origine utilisant des noms de fichiers longs. Correspond à l’arborescence dans la [table de répertoires](directory-table.md). Des privilèges élevés peuvent être nécessaires pour installer ce package.                                                                                                                                     |
| 1     | Source d’origine utilisant des noms de fichiers courts. Correspond à l’arborescence dans la [table de répertoires](directory-table.md). Des privilèges élevés peuvent être nécessaires pour installer ce package.                                                                                                                                    |
| 2     | Fichiers sources compressés utilisant des noms de fichiers longs. Correspond aux armoires et aux fichiers de la [table multimédia](media-table.md). Des privilèges élevés peuvent être nécessaires pour installer ce package.                                                                                                                   |
| 3     | Fichiers sources compressés utilisant des noms de fichiers courts. Correspond aux armoires et aux fichiers de la [table multimédia](media-table.md). Des privilèges élevés peuvent être nécessaires pour installer ce package.                                                                                                                  |
| 4     | Image administrative utilisant des noms de fichiers longs. Correspond à l’arborescence dans la [table de répertoires](directory-table.md). Des privilèges élevés peuvent être nécessaires pour installer ce package.                                                                                                                                |
| 5     | Image administrative utilisant des noms de fichiers courts. Correspond à l’arborescence dans la [table de répertoires](directory-table.md). Des privilèges élevés peuvent être nécessaires pour installer ce package.                                                                                                                               |
| 8     | Des privilèges élevés ne sont pas nécessaires pour installer ce package. Utilisez cette valeur lors [de la création de packages sans la boîte de dialogue contrôle de compte d’utilisateur](authoring-packages-without-the-uac-dialog-box.md). Disponible à partir de Windows Installer version 4,0 et Windows Vista ou Windows Server 2008.<br/> |



 

Notez que si le package est marqué comme compressé (bit 1 est défini), le Windows Installer installe uniquement les fichiers situés à la racine de la source. Dans ce cas, même les fichiers marqués comme non compressés dans la [table file](file-table.md) doivent se trouver à la racine à installer. Pour spécifier une image source qui contient à la fois un fichier CAB (fichiers compressés) et des fichiers non compressés qui correspondent à l’arborescence dans la [table Directory](directory-table.md), marquez le package comme non compressé en laissant le bit 1 unset (valeur = 0) dans la propriété **Résumé du nombre de mots** et définissez **msidbFileAttributesCompressed** (valeur = 16384) dans la colonne attributs de la [table de fichiers](file-table.md) pour

Dans une transformation, la propriété **Résumé du nombre de mots** doit avoir la valeur null.

Dans le flux d’informations de synthèse d’un package correctif, la propriété **Résumé du nombre de mots** indique la version minimale de Windows Installer requise pour installer le correctif.



| Valeur | Signification                                                                                                                                                                              |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | La valeur par défaut, qui indique que MSPATCH a été utilisé pour créer le correctif.                                                                                                        |
| 2     | Nécessite au minimum Windows Installer 1,2 pour appliquer le correctif. Un correctif avec un nombre de mots de « 2 » échoue immédiatement s’il est utilisé avec une version de Windows Installer antérieure à 1,2. |
| 3     | Nécessite au minimum Windows Installer 2,0 pour appliquer le correctif. Un correctif avec un nombre de mots de « 3 » échoue immédiatement s’il est utilisé avec une version de Windows Installer antérieure à 2,0. |
| 4     | Nécessite au minimum Windows Installer 3,0 pour appliquer le correctif. Un correctif avec un nombre de mots de « 4 » échoue s’il est utilisé avec une version de Windows Installer antérieure à 3,0.             |
| 5     | Nécessite au minimum Windows Installer 3,1 pour appliquer le correctif.                                                                                                               |



 

Cette propriété de résumé est obligatoire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Descriptions des propriétés de synthèse](summary-property-descriptions.md)
</dt> </dl>

 

 




