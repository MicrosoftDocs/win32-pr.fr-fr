---
title: Objet utilisateur Winnt
description: L’objet utilisateur Winnt représente un compte d’utilisateur dans un domaine Windows NT 4,0.
ms.assetid: c57016e2-538b-4f37-a1bb-699fcf3c080d
ms.tgt_platform: multiple
keywords:
- ADSI, objet utilisateur Winnt
- Fournisseur WinNT ADSI, objet utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50a89c2c4daf0d02e1cb9a150e35702ab4f8775f6bcc993db2b0348768bb1603
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119022997"
---
# <a name="winnt-user-object"></a>Objet utilisateur Winnt

L’objet utilisateur Winnt représente un compte d’utilisateur dans un domaine Windows NT 4,0. L’objet présente des fonctionnalités spéciales. Dans une instance, il ne prend pas en charge toutes les méthodes de propriété de l’interface [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) . Dans une deuxième instance, elle prend en charge des propriétés personnalisées qui sont accessibles uniquement avec la méthode [**IADs. obten**](/windows/desktop/api/Iads/nf-iads-iads-get) ou [**IADs. put**](/windows/desktop/api/Iads/nf-iads-iads-put) .

Pour plus d’informations sur les objets utilisateur WinNT, consultez :

-   [Propriétés IADsUser non prises en charge](unsupported-iadsuser-properties.md)
-   [Propriétés de l’utilisateur personnalisé Winnt](winnt-custom-user-properties.md)
-   [Exemples de gestion de compte d’utilisateur Winnt](winnt-user-account-management-examples.md)

 

 




