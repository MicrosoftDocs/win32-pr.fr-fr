---
description: Une fois que vous avez terminé avec une classe ou une instance, vous souhaiterez peut-être supprimer cette classe ou cette instance de WMI.
ms.assetid: 8d4bf548-a332-4058-92d0-d613bbeaa408
ms.tgt_platform: multiple
title: Suppression d’une classe ou d’une instance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42a46a52400623e31df3e051a0b587f49326733b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202294"
---
# <a name="deleting-a-class-or-instance"></a>Suppression d’une classe ou d’une instance

Une fois que vous avez terminé avec une classe ou une instance, vous souhaiterez peut-être supprimer cette classe ou cette instance de WMI. Comme d’autres technologies orientées objet, vous pouvez supprimer des objets de classe ou d’instance pour nettoyer l’espace de noms WMI et pour retourner des ressources système. Toutefois, de nombreuses classes et instances de WMI sont persistantes et utilisées par diverses applications à un moment donné. par conséquent, soyez prudent lors de la suppression d’une classe ou d’une instance WMI : votre application ou une autre application aura probablement besoin de la classe ou de l’instance à une date ultérieure.

La suppression d’une classe ou d’une instance est une procédure simple. Toutefois, en raison de la nature permanente d’une classe, vous n’aurez probablement pas besoin de supprimer une classe souvent. Par exemple, il est peu probable que vous supprimiez la classe [**Win32 \_ DiskDrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive) , car il est peu probable que vous ne disposiez pas d’un lecteur de disque au sein de votre entreprise. Au lieu de cela, vous serez plus enclin à supprimer une instance d’une classe. Pour plus d’informations, consultez [Suppression d’une instance](deleting-an-instance.md).

Bien que cela soit rare, vous pouvez être amené à mettre à jour une classe que vous avez créée. Par exemple, vous pouvez créer une classe pour représenter une application tierce. Si le logiciel tiers a mis à jour ses logiciels dans la mesure où votre classe n’est plus correctement représentée par le logiciel, vous devrez peut-être supprimer votre classe d’origine. Pour plus d’informations, consultez [Suppression d’une classe](deleting-a-class.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Conception de classes format MOF (MOF)](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 
