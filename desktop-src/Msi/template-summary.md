---
description: Pour un package d’installation, la propriété Résumé du modèle indique les versions de la plateforme et de la langue qui sont compatibles avec cette base de données d’installation.
ms.assetid: a1015ddb-8d5c-40f7-97ac-4a1347644ae6
title: Propriété Résumé du modèle
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36b3949e7028fd0b1b5f9ff3112f1a3d03c9b87e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545405"
---
# <a name="template-summary-property"></a>Propriété Résumé du modèle

Pour un package d’installation, la propriété **Résumé du modèle** indique les versions de la plateforme et de la langue qui sont compatibles avec cette base de données d’installation. La syntaxe des informations de propriétés de **Résumé du modèle** pour une base de données d’installation est la suivante :

\[*propriété de la plateforme* \] ; \[ *ID* \] \[ de langue,*ID de langue* \] \[ ,... \] .

Les exemples suivants sont des valeurs valides pour la propriété **Résumé du modèle** :

-   x64 ; 1033
-   Intel ; 1033
-   Intel64 ; 1033
-   ; 1033
-   Intel ; 1033, 2046
-   Intel64 ; 1033, 2046
-   Intel ; 0
-   ARM ; 1033, 2046
-   Arm ; 0
-   Arm64 ; 1033, 2046
-   Arm64 ; 0

La propriété **Résumé du modèle** d’une transformation indique les versions de la plateforme et de la langue compatibles avec la transformation. Dans un fichier de transformation, une seule langue peut être spécifiée. La plateforme et le langage spécifiés déterminent si une transformation peut être appliquée à une base de données particulière. La propriété de la plateforme et la propriété Language peuvent être laissées vides si aucune restriction de transformation ne s’appuie sur ces dernières pour valider la transformation.

La propriété **Résumé du modèle** d’un package correctif est une liste délimitée par des points-virgules des codes de produit pouvant accepter le correctif. Si vous utilisez [Msimsp.exe](msimsp-exe.md) et [Patchwiz.dll](patchwiz-dll.md) pour générer le package de correctifs, cette liste est obtenue à partir de la [table TargetImages](targetimages-table-patchwiz-dll-.md) du fichier de création de correctif.

Cette propriété de résumé est obligatoire.

## <a name="remarks"></a>Notes

Si la plateforme actuelle ne correspond pas à l’une des plateformes spécifiées dans la propriété **Résumé du modèle** , le programme d’installation ne traite pas le package.

Si la spécification de la plateforme est manquante dans la valeur de la propriété **Résumé du modèle** , le programme d’installation suppose l’architecture Intel.

S’il s’agit d’un package de Windows Installer 64 bits exécuté sur une plate-forme Intel64 (Itanium), entrez Intel64 dans la propriété **Résumé du modèle** .

S’il s’agit d’un package de Windows Installer 64 bits exécuté sur une plateforme x64, entrez x64 dans la propriété **Résumé du modèle** .

S’il s’agit d’un package de Windows Installer 64 bits exécuté sur une plateforme Arm64, entrez Arm64 dans la propriété **Résumé du modèle** .

Un package de Windows Installer ne peut pas être marqué comme prenant en charge à la fois Intel64 et x64 ; par exemple, la valeur de la propriété de **Résumé de modèle** Intel64, x64 n’est pas valide.

Un package Windows Installer ne peut pas être marqué comme prenant en charge les plateformes 32 bits et 64 bits ; par exemple, les valeurs de propriété de **Résumé de modèle** telles que Intel, x64 ou Intel, Intel64 ne sont pas valides.

Si vous entrez 0 (zéro) dans le champ ID de langue de la propriété **Résumé du modèle** , ou si vous laissez ce champ vide, cela indique que le package est indépendant de la langue.

S’il s’agit d’un package Windows Installer exécuté sur Windows RT, entrez la valeur ARM dans la propriété **Résumé du modèle** .

Les modules de fusion sont les seuls packages qui peuvent avoir plusieurs langues. Une seule langue peut être spécifiée dans une base de données du programme d’installation source. Pour plus d’informations, consultez [modules de fusion multilingues](multiple-language-merge-modules.md).

La plateforme alpha n’est pas prise en charge par Windows Installer.

**Windows Installer :** La syntaxe suivante n’est pas prise en charge :

\[*propriété Platform* \] \[ ,*propriété Platform* \] \[ \] ,... \[ *ID* \] \[ de langue,*ID de langue* \] \[ ,... \] .

Les exemples suivants ne sont pas des valeurs valides pour la propriété **Résumé du modèle** :

-   Alpha, Intel ; 1033
-   Intel, alpha ; 1033
-   Alpha ; 1033
-   Alpha ; 1033, 2046

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Descriptions des propriétés de synthèse](summary-property-descriptions.md)
</dt> </dl>

 

 




