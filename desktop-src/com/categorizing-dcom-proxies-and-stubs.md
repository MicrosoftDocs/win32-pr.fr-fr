---
title: Catégorisation des proxys et des stubs DCOM
description: Catégorisation des proxys et des stubs DCOM
ms.assetid: f5d117d6-6c2c-4beb-8869-1581a5b1846f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f45f61d89e31316975685d3e603a93d30559546c86abc3b63e8e7e8a0c83ff1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118310866"
---
# <a name="categorizing-dcom-proxies-and-stubs"></a>Catégorisation des proxys et des stubs DCOM

DCOM marshale les références aux objets en construisant des OBJREFs qui contiennent des CLSID. Ces CLSID sont vulnérables aux attaques de sécurité, car les dll arbitraires peuvent être chargées pendant le marshaling. Toutefois, l' \_ indicateur EOAC no \_ Custom \_ Marshal peut être spécifié lors de l’appel de [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) (consultez [**\_ \_ fonctionnalités d’authentification Eole**](/windows/win32/api/objidlbase/ne-objidlbase-eole_authentication_capabilities)). La définition de cet indicateur permet de protéger la sécurité du serveur lors de l’utilisation de DCOM, car cela réduit le risque d’exécution de dll arbitraires. Lorsque cet indicateur est défini, le serveur autorise le marshaling des CLSID uniquement qui sont implémentés dans ole32.dll, comadmin.dll, comsvcs.dll ou es.dll, ou qui implémentent l’ID de \_ catégorie de marshaleur CATID.

\_Le marshaleur CATID est un GUID de catégorie de composant qui peut être associé à un CLSID qui est en cours de marshaling personnalisé. Les interfaces en cours de marshaling personnalisé avec ce CLSID sont autorisées quand le EOAC \_ aucun \_ \_ Marshal personnalisé n’est défini via [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Catégories de composant](component-categories.md)
</dt> </dl>

 

 