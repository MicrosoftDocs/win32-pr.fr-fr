---
title: Identificateur de l’objet OBJID_QUERYCLASSNAMEIDX
description: Microsoft Active Accessibility utilise l' \_ identificateur d’objet OBJID QUERYCLASSNAMEIDX avec le \_ message WM GETOBJECT pour déterminer la classe à laquelle appartient un contrôle Windows standard ou un contrôle commun.
ms.assetid: 2167df6d-5df3-40b7-bebe-142f4bd98cd7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba7d73a152380411ef0b230de8f0e3372a6718b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010611"
---
# <a name="the-objid_queryclassnameidx-object-identifier"></a>Identificateur d' \_ objet QUERYCLASSNAMEIDX objid

Microsoft Active Accessibility utilise l’identificateur d’objet [**OBJID \_ QUERYCLASSNAMEIDX**](object-identifiers.md) avec le message [**WM \_ GETOBJECT**](wm-getobject.md) pour déterminer la classe à laquelle appartient un contrôle Windows standard ou un contrôle commun. Un contrôle répond à ce message en retournant une valeur que Microsoft Active Accessibility mappe au nom de classe du contrôle. Microsoft Active Accessibility utilise ces informations pour fournir une prise en charge de l’accessibilité pour les contrôles standard Windows et les contrôles communs.

en règle générale, seuls les contrôles de Windows standard et les contrôles communs répondent à l’identificateur d’objet [**OBJID \_ QUERYCLASSNAMEIDX**](object-identifiers.md) . toutefois, un contrôle personnalisé peut également répondre s’il comprend toutes les mêmes fonctionnalités qu’un contrôle Windows standard ou un contrôle commun existant. Cela permet au contrôle personnalisé d’être pris en charge par l’un des objets proxy standard fournis par Microsoft Active Accessibility.

Pour plus d’informations, consultez [annexe F : valeurs de l’identificateur d’objet pour objid \_ QUERYCLASSNAMEIDX](appendix-f--object-identifier-values-for-objid-queryclassnameidx.md).

 

 




