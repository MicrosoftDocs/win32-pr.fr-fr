---
title: Liaison tardive ce qui se passe en coulisses
description: Cette rubrique décrit le fonctionnement de la liaison tardive dans ADSI.
ms.assetid: f4ff19fc-d69e-4528-a6e2-2544d9149e8c
ms.tgt_platform: multiple
keywords:
- extensions ADSI, liaison tardive, ce qui se passe en coulisses
- liaison Active Directory, liaison tardive
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5299b715325e4eda88a0eeaca2b22b4bdaa15a96
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104463699"
---
# <a name="late-binding-whats-happening-under-the-hood"></a>Liaison tardive : que se passe-t-il en coulisse ?

La liste suivante décrit le processus général pour effectuer une liaison tardive :

-   Un objet est lié à un objet d’annuaire ADSI. Par exemple, « LDAP : converti = JeffSmith, OU = Sales, DC = fabrikam, DC = COM » est lié à l’aide de la liaison tardive COM. ADSI appelle alors la méthode [**QueryInterface**](/windows/win32/api/oaidl/nn-oaidl-idispatch) sur l’interface **IDispatch** .
-   ADSI recherche un objet dans la classe utilisateur et crée un objet qui prend en charge les interfaces appropriées, telles que [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser).
-   ADSI effectue une recherche dans le registre et trouve des CLSID d’extension pour l’utilisateur. N’oubliez pas que l’interface ADSI met en cache ces données.
-   Un événement effectue un appel à la méthode **MyNewMethod** . ADSI recherche son ID de dispatch et les ID de dispatch pour d’autres extensions ADSI. ADSI recherche ensuite l’extension qui sert cet appel et appelle l’interface [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) pour cette extension.
-   L’extension exécute la fonction.
-   À présent, le writer client appelle la méthode **YourNewMethod** à l’aide de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) pour l’extension actuelle. L’implémentation **IDispatch** de l’extension délègue à **IDispatch** pour ADSI.
-   [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) pour ADSI recherche à nouveau l’extension appropriée, ou elle-même, puis appelle l’extension appropriée à l’aide de l’interface [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) pour cette extension.

 

 