---
title: Création de descripteurs de sécurité pour les nouveaux objets d’annuaire
description: Vous pouvez utiliser ADSI pour créer un descripteur de sécurité et le définir en tant que propriété nTSecurityDescriptor d’un nouvel objet, ou l’utiliser pour remplacer la propriété nTSecurityDescriptor d’un objet existant.
ms.assetid: b9ff626f-17f1-4fc1-9d6e-4f47e29a5aeb
ms.tgt_platform: multiple
keywords:
- Création d’un descripteur de sécurité pour un nouvel objet annuaire AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78265d27c52023d669e27fc9890fd2d5273e2ffd
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104462899"
---
# <a name="creating-security-descriptors-for-new-directory-objects"></a>Création de descripteurs de sécurité pour les nouveaux objets d’annuaire

Vous pouvez utiliser ADSI pour créer un descripteur de sécurité et le définir en tant que propriété **ntSecurityDescriptor** d’un nouvel objet, ou l’utiliser pour remplacer la propriété **ntSecurityDescriptor** d’un objet existant.

Pour créer un descripteur de sécurité pour un objet :

1.  Utilisez [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour créer l’objet com ADSI pour le nouveau descripteur de sécurité et obtenir un pointeur d’interface [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) vers cet objet. N’oubliez pas que l’ID de classe est le **\_ SecurityDescriptor CLSID**.
2.  Utilisez la méthode [**IADsSecurityDescriptor ::p ut \_ owner**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) pour définir le propriétaire de l’objet. Le tiers de confiance est un utilisateur, un groupe ou un autre principal de sécurité. Une application doit utiliser la valeur de la propriété appropriée de l’objet utilisateur ou groupe du tiers de confiance auquel appliquer l’entrée du contrôle d’accès.
3.  Utilisez la méthode de [**\_ contrôle IADsSecurityDescriptor ::p ut**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) pour contrôler si les listes DACL et les listes SACL sont héritées par l’objet de son conteneur parent.
4.  Utilisez [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour créer l’objet com ADSI pour la liste DACL pour le nouveau descripteur de sécurité et obtenir un pointeur d’interface [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist) vers cet objet. N’oubliez pas que l’ID de classe est **CLSID \_ AccessControlList**.
5.  Pour chaque entrée du contrôle d’accès à ajouter à la liste DACL, utilisez [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour créer l’objet com ADSI pour la nouvelle entrée du contrôle d’accès et obtenir un pointeur d’interface [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) vers cet objet. N’oubliez pas que l’ID de classe est CLSID \_ AccessControlEntry.
6.  Pour chaque entrée du contrôle d’accès à ajouter à la liste DACL, définissez les propriétés de l’entrée du contrôle d’accès à l’aide des méthodes de propriété de l’objet [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) de l’ACE. Pour plus d’informations sur les propriétés à définir sur une entrée du contrôle d’accès, consultez [définition des droits d’accès sur un objet](setting-access-rights-on-an-object.md).
7.  Pour chaque entrée du contrôle d’accès à ajouter à la liste DACL, utilisez la méthode **QueryInterface** sur l’objet [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) pour obtenir un pointeur [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . La méthode [**IADsAccessControlList :: AddAce**](/windows/desktop/api/iads/nf-iads-iadsaccesscontrollist-addace) requiert un pointeur d’interface **IDISPATCH** vers l’entrée du contrôle d’accès.
8.  Pour chaque entrée du contrôle d’accès à ajouter à la liste DACL, utilisez [**IADsAccessControlList :: AddAce**](/windows/desktop/api/iads/nf-iads-iadsaccesscontrollist-addace) pour ajouter la nouvelle entrée du contrôle d’accès à la liste DACL. N’oubliez pas que l’ordre des ACE dans la liste de contrôle d’accès peut affecter l’évaluation de l’accès à l’objet. Pour un accès correct à l’objet, vous devrez peut-être créer une nouvelle liste de contrôle d’accès, ajouter les entrées de contrôle d’accès de l’ACL existante dans l’ordre approprié à la nouvelle liste de contrôle d’accès, puis remplacer l’ACL existante dans le descripteur de sécurité par la nouvelle liste de contrôle d’accès. Pour plus d’informations, consultez [ordre des entrées de commande dans une liste DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).
9.  Suivez les étapes 4-8 pour créer la liste SACL pour le nouveau descripteur de sécurité.
10. Utilisez la méthode [**IADsSecurityDescriptor ::p ut \_ DiscretionaryAcl**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) pour définir la liste DACL. Pour plus d’informations sur les DACL, consultez [DACL null et listes DACL vides](null-dacls-and-empty-dacls.md).
11. Utilisez la méthode [**IADsSecurityDescriptor ::p ut \_ SystemAcl**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) pour définir la liste SACL.
12. Convertissez l’objet [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) en [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) à l’aide de la méthode **QueryInterface** de l’objet **IADsSecurityDescriptor** pour obtenir une interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . Définissez ensuite le membre **VT** du **Variant** sur **VT \_ Dispatch** et définissez le membre **pdispVal** de la **variante** comme étant égal au pointeur **IDispatch** .
13. Obtient un pointeur d’interface [**IADs**](/windows/desktop/api/iads/nn-iads-iads) vers l’objet.
14. Utilisez la méthode [**IADs ::P ut**](/windows/desktop/api/iads/nf-iads-iads-put) avec « ntSecurityDescriptor » et la [**variante**](/windows/win32/api/oaidl/ns-oaidl-variant) créée ci-dessus pour écrire le nouveau descripteur de sécurité dans le cache de propriétés.
15. Utilisez la méthode [**IADs :: setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) pour mettre à jour la propriété sur l’objet dans le répertoire.

 

 