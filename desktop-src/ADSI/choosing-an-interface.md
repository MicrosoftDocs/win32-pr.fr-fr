---
title: Choix d’une interface pour la liaison
description: Lorsqu’un objet d’annuaire est lié à, l’appelant spécifie le type d’interface ADSI souhaité.
ms.assetid: 3c86e136-6d82-4baf-9c76-27dac8ad68ac
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, utilisation de, choix d’une interface pour la liaison
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15dfb1f39a24f6113796ed81d5a3269cfc2134d8d68546170049dd2f8a70bb0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118180293"
---
# <a name="choosing-an-interface-for-binding"></a>Choix d’une interface pour la liaison

Lorsqu’un objet d’annuaire est lié à, l’appelant spécifie le type d’interface ADSI souhaité. Tous les objets d’annuaire ADSI prennent en charge l’interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) . Un objet ADSI peut également prendre en charge d’autres interfaces. Les interfaces réelles prises en charge par l’objet dépendent de la classe de l’objet. Par exemple, un objet utilisateur prend en charge l’interface [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) , mais ne prend pas en charge l’interface [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer) .

Les clients Automation doivent utiliser les interfaces **IADs \** _, car ces interfaces sont des interfaces doubles qui fournissent un niveau supérieur d’abstraction et fournissent des données à l’aide du type de données [_ *Variant* *](/windows/win32/api/oaidl/ns-oaidl-variant) .

Outre les interfaces **IADs \** _, les clients C/C++ peuvent utiliser les interfaces [_ *IDirectoryObject* *](/windows/desktop/api/Iads/nn-iads-idirectoryobject) et [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) . Ces interfaces ne sont pas des interfaces doubles et ne prennent pas en charge Automation. Ces interfaces permettent de mieux contrôler les attributs à récupérer et d’autoriser l’accès aux données brutes stockées dans une propriété. Par exemple, lorsque la méthode [**IADs :: obten**](/windows/desktop/api/Iads/nf-iads-iads-get) est utilisée pour récupérer l' **attribut ntSecurityDescriptor** d’un objet, la méthode **IADs :: obtenir** fournit un pointeur d’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) qui prend en charge l’interface [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) . L’interface **IADsSecurityDescriptor** est fournie par ADSI pour représenter un descripteur de sécurité. En comparaison, lorsque la méthode [**IDirectoryObject :: GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) est utilisée pour récupérer l’attribut **ntSecurityDescriptor** , **IDirectoryObject :: GetObjectAttributes** fournit un tableau d’octets qui peut être casté en une structure de [**\_ descripteur de sécurité**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) . Les API de sécurité Win32 peuvent être utilisées avec ces données pour manipuler le descripteur de sécurité.

 

 