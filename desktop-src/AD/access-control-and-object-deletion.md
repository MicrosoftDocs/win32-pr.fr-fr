---
title: Access Control et suppression d’objets
description: Active Directory vous permet de supprimer un objet si vous avez la possibilité de supprimer l’accès à l’objet ou aux publicités \_ droit \_ DS \_ supprimer \_ l’accès enfant au type d’objet sur le conteneur parent.
ms.assetid: 87027c25-e3c9-4bad-8df3-cb6205e40ef6
ms.tgt_platform: multiple
keywords:
- AD Access Control et suppression d’objets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bddcd2b563e144743689f2a26c17bd417db14ee
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724373"
---
# <a name="access-control-and-object-deletion"></a>Access Control et suppression d’objets

Active Directory Domain Services vous permettent de supprimer un objet si vous disposez de l’un des droits d’accès suivants :

-   SUPPRIMER l’accès à l’objet lui-même
-   AD \_ Right \_ DS \_ Supprimer l' \_ accès enfant pour ce type d’objet sur le conteneur parent

N’oubliez pas que le système vérifie le descripteur de sécurité pour l’objet et son parent avant de refuser la suppression. Cela signifie qu’une entrée du contrôle d’accès qui refuse explicitement l’accès en suppression à un utilisateur n’a aucun effet si l’utilisateur a supprimé l' \_ accès enfant sur le parent. De même, une entrée du contrôle d’accès qui refuse l' \_ accès à la suppression d’un enfant sur le parent peut être remplacée si l’accès en suppression est autorisé sur l’objet lui-même.

Pour effectuer une opération de suppression d’arborescence, par exemple à l’aide de la méthode [**IADsDeleteOps ::D eleteobject**](/windows/desktop/api/iads/nf-iads-iadsdeleteops-deleteobject) , vous devez disposer des \_ services de domaine Active \_ Directory droit supprimer l' \_ \_ accès à l’arborescence pour l’objet. Si vous disposez de ce droit d’accès, vous pouvez supprimer l’objet et tous les objets enfants, quelles que soient les protections sur les objets enfants. Pour supprimer une arborescence si vous n’avez pas d' \_ \_ accès à la suppression de l’arborescence des services de domaine Active Directory \_ \_ , vous devez parcourir de manière récursive l’arborescence, en supprimant chaque objet individuellement. Dans ce cas, vous devez disposer de l’accès de suppression ou de suppression \_ d’enfant nécessaire pour chaque objet de l’arborescence.

> [!WARNING]
> Si les utilisateurs disposent d’un \_ droit de \_ Suppression d’arborescence des services de domaine Active Directory \_ \_ pour un objet, ils peuvent supprimer l’intégralité d’une sous-arborescence, y compris tous les objets enfants. Pour cette raison, vous pouvez envisager de révoquer l’autorisation d’accès « supprimer la sous-arborescence » pour tous les utilisateurs sur un conteneur parent.

 

 

 