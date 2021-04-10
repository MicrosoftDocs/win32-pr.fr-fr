---
title: Lecture d’un droit d’accès de contrôle défini dans l’ACL d’un objet
description: Les propriétés de l’interface IADsAccessControlEntry sont utilisées pour accorder ou refuser des droits d’accès de contrôle.
ms.assetid: 2c6fef91-990e-4954-9aff-c9ec72d13972
ms.tgt_platform: multiple
keywords:
- Lecture d’un droit d’accès de contrôle défini dans l’ACL d’un objet Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4877c96a95fc94095c79ad129e8a07b1c786abe1
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104030991"
---
# <a name="reading-a-control-access-right-set-in-an-objects-acl"></a>Lecture d’un droit d’accès de contrôle défini dans l’ACL d’un objet

À l’aide d’ADSI, vous lisez une entrée de contrôle d’accès de contrôle comme vous le feriez pour n’importe quelle autre entrée de contrôle d’accès. Sachez que vous pouvez également utiliser les API de sécurité Win32 pour lire les ACL sur les objets d’annuaire. Toutefois, les droits d’accès de contrôle utilisent les propriétés de l’interface [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) de manière à accorder et refuser des droits d’accès au contrôle :

-   [**AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) doit contenir **les \_ droits \_ d' \_ \_ accès au contrôle d’annuaire Active Directory**.
-   La valeur [**Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) est le **type d' \_ objet indicateur ADS \_ \_ \_ présent**.
-   [**ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) est le format de chaîne de l’attribut **rightsGUID** du droit d’accès au contrôle. Le format de chaîne du GUID est le même que celui de la fonction de bibliothèque COM [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) .
-   [**AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) est soit **ADS \_ AceType \_ Access \_ allowed \_ Object** pour accorder au tiers de confiance le droit d’accès du contrôle, soit l' **\_ objet ADS AceType \_ accès \_ refusé \_** pour refuser au tiers de confiance le droit d’accès au contrôle.
-   Le [**tiers de confiance**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) est le principal de sécurité ; Il s’agit de l’utilisateur, du groupe, de l’ordinateur, et ainsi de suite, à laquelle l’entrée du contrôle d’accès s’applique.

Utilisez la procédure suivante pour lire une entrée du contrôle d’accès pour un objet ADSI. La procédure suivante s’applique aux applications C et C++.

**Pour lire une entrée du contrôle d’accès pour un objet ADSI**

1.  Obtient un pointeur d’interface [**IADs**](/windows/desktop/api/iads/nn-iads-iads) vers l’objet.
2.  Utilisez la méthode [**IADs :: obten**](/windows/desktop/api/iads/nf-iads-iads-get) pour récupérer le descripteur de sécurité de l’objet. Le nom de la propriété qui contient le descripteur de sécurité est « nTSecurityDescriptor ». La propriété est retournée en tant que **Variant** qui contient un pointeur [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . N’oubliez pas que le membre **VT** est **VT \_ Dispatch**. Appelez **QueryInterface** sur ce pointeur **IDispatch** pour qu’une interface [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) utilise les méthodes sur cette interface pour accéder à la liste de contrôle d’accès du descripteur de sécurité.
3.  Utilisez la méthode [**IADsSecurityDescriptor :: obten \_ DiscretionaryAcl**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) pour accéder à la liste de contrôle d’accès. La méthode retourne un pointeur [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . Appelez **QueryInterface** sur ce pointeur **IDispatch** pour qu’une interface [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist) utilise les méthodes sur cette interface pour accéder aux ACE individuelles dans la liste de contrôle d’accès.
4.  Utilisez la méthode [**IADsAccessControlList :: obten \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadsaccesscontrollist-get__newenum) pour énumérer les ACE. La méthode retourne un pointeur [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . Appelez **QueryInterface** sur ce pointeur **IUnknown** pour récupérer une interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) .
5.  Utilisez la méthode [**IEnumVARIANT :: Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) pour énumérer les ACE dans la liste de contrôle d’accès. La propriété est retournée en tant que **Variant** qui contient un pointeur [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . N’oubliez pas que le membre **VT** est **VT \_ Dispatch**. Appelez **QueryInterface** sur ce pointeur **IDispatch** pour obtenir une interface [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) pour lire l’entrée du contrôle d’accès.
6.  Appelez la [**méthode IADsAccessControlEntry :: \_ obtenir AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) pour obtenir le **AccessMask** et vérifier que la valeur **AccessMask** pour l’indicateur d' **\_ \_ \_ \_ accès au contrôle de service d’annuaire AD Right** . S’il a cet indicateur, l’ACE contient un droit d’accès de contrôle.
7.  Appelez la méthode [**IADsAccessControlEntry :: obtenir \_ Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) pour obtenir l’indicateur pour le type d’objet.
8.  Valeur de la case à cocher Vérifier la valeur des [**indicateurs**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) pour les **annonces de type indicateur \_ \_ \_ \_ présent** . Si la valeur **Flags** est définie sur le **\_ \_ type d’objet indicateur \_ \_ ADS**, appelez la méthode **IADsAccessControlEntry :: obtenir \_ ObjectType** pour obtenir une chaîne qui contient le RIGHTSGUID du droit d’accès du contrôle auquel s’applique l’entrée du contrôle d’accès.
9.  Appelez la méthode [**IADsAccessControlEntry :: obten \_ AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) pour accéder au type d’entrée du contrôle d’accès. Le type sera un **objet ad \_ ACETYPE \_ Access \_ allowed \_** pour accorder au tiers de confiance le droit d’accès du contrôle ou l' **\_ objet ad ACETYPE \_ Access \_ denied \_** pour refuser le droit d’accès au contrôle.
10. Appelez la méthode [**IADsAccessControlEntry :: obtient le \_ tiers de confiance**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) pour accéder au principal de sécurité, c’est-à-dire à l’utilisateur, au groupe, à l’ordinateur, etc. auquel s’applique l’entrée du contrôle d’accès.
11. Lorsque vous avez terminé avec les chaînes [**ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) et **fiduciaire** , utilisez [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) pour libérer la mémoire pour ces chaînes.
12. Lorsque vous avez terminé avec les interfaces, appelez **Release** pour décrémenter ou libérer toutes les références d’interface.

 

 