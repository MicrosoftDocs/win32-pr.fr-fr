---
description: Dans WMI, une classe est un objet qui décrit certains aspects d’une entreprise, tels qu’un type spécial de lecteur de disque.
ms.assetid: 06b75910-f126-48b6-8e43-4a9ed4661732
ms.tgt_platform: multiple
title: Création d’une classe WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec2db62f1f0d14035f7bcc3fd74f8bbbfbacf08cb0dbf139b06c9870b7039e19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612559"
---
# <a name="creating-a-wmi-class"></a>Création d’une classe WMI

Dans WMI, une classe est un objet qui décrit certains aspects d’une entreprise, tels qu’un type spécial de lecteur de disque. Après avoir créé une définition de classe, écrivez votre DLL de fournisseur pour fournir des instances de la classe, des données de propriété et des méthodes d’exécution définies pour la classe. Les scripts et les applications peuvent ensuite obtenir des données ou contrôler l’appareil. Pour plus d’informations, consultez [développement d’un fournisseur WMI](developing-a-wmi-provider.md).

> [!Note]  
> Pour vous assurer que toutes les définitions de classe WMI pour les objets managés sont restaurées dans l' [*espace de stockage WMI*](gloss-w.md) en cas d’échec et de redémarrage de WMI, utilisez l’instruction de préprocesseur de l’instruction de [**\# récupération automatique pragma**](pragma-autorecover.md) dans votre fichier MOF.

 

## <a name="base-class"></a>Classe de base

Une classe de base représente un concept général. Par exemple, la classe [**CIM \_ CDROMDrive**](/windows/desktop/CIMWin32Prov/cim-cdromdrive) représente tous les types de lecteurs de CD-ROM dans WMI et contient des propriétés générales qui décrivent tous les types de lecteurs de CD-ROM. Pour plus d’informations, consultez [création d’une classe de base](creating-a-base-class.md).

Une classe dérivée hérite des propriétés et des méthodes d’une autre classe. Une classe dérivée représente généralement un cas spécifique d’une classe de base. par exemple, la classe [**Win32 \_ CDROMDrive**](/windows/desktop/CIMWin32Prov/win32-cdromdrive) représente un lecteur de CD-rom sur un système Windows. La classe **Win32 \_ CDROMDrive** est basée sur et hérite de nombreuses propriétés de [**CIM \_ CDROMDrive**](/windows/desktop/CIMWin32Prov/cim-cdromdrive). Toutefois, **les \_ CDROMDrive Win32**, comme d’autres classes dérivées, peuvent avoir des propriétés supplémentaires qui rendent la classe dérivée unique. Pour plus d’informations, consultez [création d’une classe dérivée](creating-a-derived-class.md).

## <a name="properties-and-methods"></a>Propriétés et méthodes

La création d’une classe signifie la définition des propriétés qui décrivent cette classe. Vous pouvez également définir des méthodes qui manipulent l’objet représenté par la classe.

En général, une propriété représente un aspect de l’objet, tel qu’un numéro de série pour un appareil ou une taille en octets pour un processus, tandis qu’une méthode représente une action qui modifie l’État ou le comportement de l’appareil ou de l’entité logique.

Chaque classe doit avoir au moins une propriété de clé. Alors qu’une classe peut avoir plusieurs clés, vous ne pouvez pas créer une instance d’une classe avec plus de 256 clés.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Conception de classes format MOF (MOF)](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 
