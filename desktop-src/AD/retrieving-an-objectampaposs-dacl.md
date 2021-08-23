---
title: Récupération de la liste DACL d’un objet
description: Le descripteur de sécurité d’un objet peut contenir une liste de contrôle d’accès discrétionnaire (DACL, Discretionary Access Control List).
ms.assetid: 93b16094-9923-4886-804f-4e989fbf6977
ms.tgt_platform: multiple
keywords:
- PUBLICITÉ DACL
- PUBLICITÉ DACL, récupération de la liste DACL d’un objet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b515e6c5d28be7003734510300fc7f6d2de776b479b56e62ad521567c76dce4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025107"
---
# <a name="retrieving-an-objects-dacl"></a>Récupération de la liste DACL d’un objet

Le descripteur de sécurité d’un objet peut contenir une liste de contrôle d’accès discrétionnaire (DACL, Discretionary Access Control List). Une liste DACL contient zéro, une ou plusieurs entrées de contrôle d’accès (ACE) qui identifient les utilisateurs et les groupes qui peuvent accéder à l’objet. Si une liste DACL est vide (autrement dit, elle ne contient aucune ACE), aucun accès n’est accordé explicitement, de sorte que l’accès est refusé implicitement. Toutefois, si le descripteur de sécurité d’un objet n’a pas de liste DACL, l’objet n’est pas protégé et tout le monde dispose d’un accès complet.

Pour récupérer la liste DACL d’un objet, vous devez être le propriétaire de l’objet ou avoir accès **en lecture au \_ contrôle** de l’objet.

Pour obtenir et définir la liste DACL d’un objet d’annuaire, utilisez l’interface [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) . À l’aide de C++, la méthode [**IADsSecurityDescriptor :: obten \_ DiscretionaryAcl**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) retourne un pointeur [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . Appelez **QueryInterface** sur ce pointeur **IDispatch** pour accéder à une interface [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist) et utilisez les méthodes sur cette interface pour accéder aux ACE individuelles dans la liste DACL. La procédure de modification d’une liste DACL est décrite dans [définition des droits d’accès sur un objet](setting-access-rights-on-an-object.md).

Pour énumérer les ACE, utilisez la méthode [**IADsAccessControlList :: obten \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadsaccesscontrollist-get__newenum) . La méthode retourne un pointeur [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . Appelez **QueryInterface** sur ce pointeur **IUnknown** pour récupérer une interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) . Utilisez la méthode [**IEnumVARIANT :: Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) pour énumérer les ACE dans la liste de contrôle d’accès. Chaque entrée du contrôle d’accès est renvoyée en tant que **Variant** contenant un pointeur [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) (le membre **VT** est **VT \_ Dispatch**). Appelez **QueryInterface** sur ce pointeur **IDispatch** pour obtenir une interface [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) pour l’entrée du contrôle d’accès. Vous pouvez utiliser les méthodes de l’interface **IADsAccessControlEntry** pour définir ou récupérer les composants d’une entrée du contrôle d’accès.

Pour plus d’informations sur les DACL et les ACE, consultez les rubriques suivantes dans le kit de développement logiciel (SDK) de la plateforme.

-   [Listes de contrôle d’accès (ACL)](/windows/desktop/SecAuthZ/access-control-lists)
-   [Entrées de contrôle d’accès (ACE)](/windows/desktop/SecAuthZ/access-control-entries)

 

 