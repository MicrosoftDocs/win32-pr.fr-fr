---
description: La définition de la stratégie TransformsSecure sur 1 informe le programme d’installation que les transformations doivent être mises en cache localement sur l’ordinateur de l’utilisateur dans un emplacement où l’utilisateur ne dispose pas d’un accès en écriture.
ms.assetid: 4fe992ed-1e8c-4ee2-a325-138bdc039e44
title: Stratégie TransformsSecure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6300a25db8e80003ff2a03afd56b168b9697f92764f16a26e99860c0a27796bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500293"
---
# <a name="transformssecure-policy"></a>Stratégie TransformsSecure

La définition de la stratégie TransformsSecure sur 1 informe le programme d’installation que les transformations doivent être mises en cache localement sur l’ordinateur de l’utilisateur dans un emplacement où l’utilisateur ne dispose pas d’un accès en écriture. La définition de cette stratégie est identique à la définition de la [propriété TRANSFORMSSECURE](transformssecure.md) , sauf que l’étendue est différente. La définition de la stratégie TransformsSecure s’applique à tous les packages installés sur un ordinateur donné. La définition de la propriété TRANSFORMSSECURE s’applique au package, quel que soit l’ordinateur.

l’objectif de cette stratégie est de fournir un stockage de transformation sécurisé avec les utilisateurs itinérants de Windows 2000. à partir de Windows Server 2003, la valeur par défaut de cette stratégie est 1.

Lorsque cette stratégie est définie, une [installation de maintenance](maintenance-installation.md) peut uniquement utiliser la transformation à partir du cache sécurisé. Dans le cas où le programme d’installation détecte que la transformation est manquante sur l’ordinateur local, le programme d’installation tente de restaurer la transformation. Pour que le programme d’installation puisse restaurer la transformation, la transformation sécurisée doit résider sur une source autorisée dans la liste source du package d’installation. Pour plus d’informations, consultez [résilience source](source-resiliency.md). L’installation de la maintenance échoue si la transformation n’est pas disponible ou ne peut pas être chargée.

sur Windows Server 2003, si cette stratégie n’est pas définie, le comportement par défaut consiste à stocker les transformations dans un emplacement sécurisé. sur toutes les versions antérieures à Windows Server 2003, si la stratégie n’est pas définie, le comportement par défaut consiste à stocker les transformations dans le profil utilisateurs.

Pour plus d’informations, consultez également la section [transformations sécurisées](secured-transforms.md) .

Windows Le programme d’installation interprète la [stratégie TransformsAtSource](transformsatsource-policy.md) comme étant identique à la stratégie TransformsSecure.

## <a name="registry-key"></a>Clé de Registre

**HKEY \_ \_** \\ **stratégies logicielles** de l’ordinateur LOCAL \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Type de données

**\_valeur DWORD reg**

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[non pris en charge dans Windows Installer 2,0 et versions antérieures](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



