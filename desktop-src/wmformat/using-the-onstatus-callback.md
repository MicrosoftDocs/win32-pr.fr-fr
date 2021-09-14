---
title: Utilisation du rappel OnStatus
description: Utilisation du rappel OnStatus
ms.assetid: 598e2d13-709b-42a3-ae06-b8c7d208ca9e
keywords:
- Windows Media Format SDK, méthode de rappel OnStatus
- Windows Media Format SDK, interface IWMStatusCallback
- OnStatus, méthode de rappel, à propos de
- IWMStatusCallback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56e96b8d7fd75fd8a1d97a56c8b09304c51d0238
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404456"
---
# <a name="using-the-onstatus-callback"></a>Utilisation du rappel OnStatus

la méthode de rappel [**IWMStatusCallback :: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) est appelée par plusieurs objets dans le kit de développement logiciel (SDK) de Format multimédia Windows. **OnStatus** reçoit des messages qui représentent des modifications de l’état des opérations du kit de développement logiciel (SDK).

Pour utiliser la méthode de rappel **OnStatus** , vous devez implémenter dans votre application une classe qui hérite de l’interface [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) . Incluez le code de votre version de **OnStatus** dans la classe. Vous trouverez plusieurs exemples d’implémentations de **OnStatus** dans les exemples inclus dans ce kit de développement logiciel (SDK). Pour plus d’informations sur les exemples, consultez [exemples d’applications](sample-applications.md).

vous devez associer votre implémentation du rappel d’état à différents objets du kit de développement logiciel (SDK) de Format de média Windows. Chaque objet a une façon différente de créer cette association. Pour obtenir la liste des méthodes qui associent des objets spécifiques, consultez la page de référence **IWMStatusCallback** .

Les messages d’État qui peuvent être reçus par **OnStatus** sont définis dans le type d’énumération d' [**\_ État WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) .

Vous pouvez choisir les messages à intercepter et ceux à ignorer. Toutefois, il est nécessaire de répondre à certains messages d’État pour certaines fonctionnalités. Par exemple, lors de l’utilisation du lecteur asynchrone, la méthode [**IWMReader :: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) ouvre un fichier de façon asynchrone. La seule façon de savoir à quel moment le fichier a été ouvert consiste à intercepter le \_ message MWT ouvert. En règle générale, les messages auxquels vous répondez sont des notifications de l’achèvement des tâches asynchrones.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Utilisation des méthodes de rappel**](using-the-callback-methods.md)
</dt> </dl>

 

 




