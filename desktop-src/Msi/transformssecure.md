---
description: L’affectation de la valeur 1 à la propriété TRANSFORMSSECURE informe le programme d’installation que les transformations doivent être mises en cache localement sur l’ordinateur de l’utilisateur dans un emplacement où l’utilisateur ne dispose pas d’un accès en écriture.
ms.assetid: 414025c3-7b83-42c7-9954-7393fba06061
title: Propriété TRANSFORMSSECURE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7af3432b8f895d4d9f5d0fe643ef8106e01e28ad64fb2db177e968fbc13d88de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118141632"
---
# <a name="transformssecure-property"></a>Propriété TRANSFORMSSECURE

L’affectation de la valeur 1 à la propriété **TRANSFORMSSECURE** informe le programme d’installation que les transformations doivent être mises en cache localement sur l’ordinateur de l’utilisateur dans un emplacement où l’utilisateur ne dispose pas d’un accès en écriture. La définition de cette propriété est semblable à la définition de la [stratégie TransformsSecure](transformssecure-policy.md) , à ceci près que l’étendue est différente. La définition de la stratégie TransformsSecure s’applique à tous les packages installés par un utilisateur donné. La définition de la propriété **TRANSFORMSSECURE** s’applique au package, quel que soit l’utilisateur.

l’objectif de cette propriété est de fournir un stockage de transformation sécurisé avec les utilisateurs itinérants de Windows 2000. Lorsque cette propriété est définie, une [installation de maintenance](maintenance-installation.md) peut uniquement utiliser la transformation à partir du chemin d’accès spécifié. Si le chemin d’accès n’est pas disponible, l’installation de la maintenance échoue. Une source pour chaque transformation sécurisée doit donc résider à l’emplacement de la source du package d’installation. Puis, si le programme d’installation détecte que la transformation est manquante sur l’ordinateur local, il peut restaurer la transformation à partir de cette source.

## <a name="remarks"></a>Remarques

Windows Le programme d’installation interprète la propriété [**TRANSFORMSATSOURCE**](transformsatsource.md) comme étant identique à la propriété **TRANSFORMSSECURE** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> <dt>

[Transformations de base de données](database-transforms.md)
</dt> </dl>

 

 




