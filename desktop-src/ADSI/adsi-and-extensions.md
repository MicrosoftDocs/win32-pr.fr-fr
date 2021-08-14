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
ms.openlocfilehash: 6f1b5a806812fea1191ce5eb1b5a977fc430d9cbf15140b4b096dbf388c85315
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118181160"
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

 

 