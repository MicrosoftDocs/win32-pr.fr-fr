---
title: Implémentation de Active Accessibility Native
description: Les éléments d’interface utilisateur qui implémentent l’interface IAccessible sont dits pour fournir une implémentation native.
ms.assetid: 36a5c0cd-53f0-433e-8932-da7d1de177dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5f6e6b6152c2f5e5c41a6a2b7cd3f84a3fce373
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010677"
---
# <a name="native-active-accessibility-implementation"></a>Implémentation de Active Accessibility Native

Les éléments d’interface utilisateur qui implémentent l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) sont dits pour fournir une *implémentation native*. Bien que le coût de développement de l’implémentation de **IAccessible** (ou de toute autre interface com) peut être élevé, l’avantage est le contrôle total des informations exposées aux clients.

Si votre application utilise des contrôles personnalisés ou d’autres contrôles qui ne peuvent pas être proxyés par Oleacc.dll, vous devrez fournir une implémentation native.

 

 




