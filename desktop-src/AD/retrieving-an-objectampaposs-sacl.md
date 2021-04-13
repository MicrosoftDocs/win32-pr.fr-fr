---
title: Récupération de la liste SACL d’un objet
description: Le descripteur de sécurité d’un objet dans Active Directory Domain Services peut contenir une liste de contrôle d’accès système (SACL).
ms.assetid: b1da91a2-d9b0-48a3-9de5-1e588209032d
ms.tgt_platform: multiple
keywords:
- AD SACL
- AD SACL, récupération de la liste SACL d’un objet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 537846f2080aecdab8e22f5fce5bdfa36298fb74
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104314610"
---
# <a name="retrieving-an-objects-sacl"></a>Récupération de la liste SACL d’un objet

Le descripteur de sécurité d’un objet dans Active Directory Domain Services peut contenir une liste de contrôle d’accès système (SACL). Une liste SACL contient des entrées de contrôle d’accès (ACE) qui spécifient les types de tentatives d’accès qui génèrent des enregistrements d’audit dans le journal des événements de sécurité d’un contrôleur de domaine. N’oubliez pas qu’une liste SACL génère des entrées de journal uniquement sur le contrôleur de domaine où la tentative d’accès a eu lieu, et non sur chaque contrôleur de domaine contenant un réplica de l’objet.

Pour définir ou récupérer la liste SACL à partir d’un descripteur de sécurité d’objet, le privilège de **\_ \_ nom de sécurité se** doit être activé dans le jeton d’accès du thread demandeur. Le groupe administrateurs dispose de ce privilège par défaut, et il peut être attribué à d’autres utilisateurs ou groupes. Pour plus d’informations, consultez [droit d’accès SACL](/windows/desktop/SecAuthZ/sacl-access-right).

Pour obtenir et définir la liste SACL d’un objet d’annuaire, utilisez l’interface [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) . À l’aide de C++, la méthode [**IADsSecurityDescriptor :: obten \_ SystemAcl**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) retourne un pointeur [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . Appelez **QueryInterface** sur ce pointeur **IDispatch** pour accéder à une interface [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist) et utilisez les méthodes sur cette interface pour accéder aux ACE individuelles dans la liste SACL. Pour plus d’informations sur la procédure de modification d’une liste SACL, qui est similaire à celle de la modification d’une liste DACL, consultez [définition des droits d’accès sur un objet](setting-access-rights-on-an-object.md).

Pour énumérer les ACE dans une liste SACL, utilisez la méthode [**IADsAccessControlList :: obtenir \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadsaccesscontrollist-get__newenum) , qui retourne un pointeur [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . Appelez **QueryInterface** sur ce pointeur **IUnknown** pour récupérer une interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) . Utilisez la méthode [**IEnumVARIANT :: Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) pour énumérer les ACE dans la liste de contrôle d’accès. Chaque entrée du contrôle d’accès est retournée en tant que **Variant** qui contient un pointeur [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) ; n’oubliez pas que le membre **VT** est **VT \_ Dispatch**. Appelez **QueryInterface** sur ce pointeur **IDispatch** pour obtenir une interface [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) pour l’entrée du contrôle d’accès. Utilisez les méthodes de l’interface **IADsAccessControlEntry** pour définir ou récupérer les composants d’une entrée du contrôle d’accès.

Pour plus d’informations sur les listes SACL, consultez :

-   [Listes de contrôle d’accès (ACL)](/windows/desktop/SecAuthZ/access-control-lists)
-   [Génération de l’audit](/windows/desktop/SecAuthZ/audit-generation)

 

 