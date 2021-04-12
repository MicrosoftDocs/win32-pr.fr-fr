---
title: Comment ADSI intègre les extensions
description: Instructions qui décrivent comment ADSI interagit avec les extensions.
ms.assetid: 00301551-ec56-4cb4-8e77-264c3ad48814
ms.tgt_platform: multiple
keywords:
- ADSI des extensions
- ADSI et extensions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 956a76954851ea54b4eae99bfa45102a3b2fefa5
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104031853"
---
# <a name="how-adsi-integrates-extensions"></a>Comment ADSI intègre les extensions

Les instructions suivantes décrivent comment ADSI interagit avec les extensions :

-   Un objet est lié à un objet d’annuaire ADSI. Par exemple, « LDAP : analyseur = JeffSmith, OU = Sales, DC = fabrikam, DC = COM ».
-   ADSI identifie que l’objet se trouve dans la classe **utilisateur** .
-   ADSI effectue une recherche dans le registre et identifie les CLSID d’extension pour l' **utilisateur**. N’oubliez pas que l’interface ADSI met en cache ces données.
-   Un événement appelle la méthode **QueryInterface** pour IID \_ IMyExtension. ADSI recherche les interfaces associées à l’objet **utilisateur** , en commençant par ses propres interfaces, puis en examinant les interfaces d’extension.
-   Si une correspondance est trouvée, ADSI crée une instance du composant qui prend en charge IID \_ IMyExtension et appelle **QueryInterface** pour l’extension. L’interface résultante est retournée.
-   L’utilisateur utilise cette interface pour appeler les méthodes d’interface.
-   Ensuite, le client appelle **QueryInterface** pour IID \_ IYourExtension, qui se trouve dans un autre composant. Ce composant délègue cet appel **QueryInterface** à l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) de l’agrégateur, qui devient ADSI lui-même.
-   Là encore, ADSI recherche les interfaces et crée l’instance de composant.

 

 