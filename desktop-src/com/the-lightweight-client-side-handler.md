---
title: Gestionnaire de Client-Side léger
description: Les gestionnaires légers côté client vous permettent de créer des gestionnaires généraux côté client de toutes tailles, pour vous aider à effectuer n’importe quel type de tâche standard.
ms.assetid: b712237c-55d7-4f52-9cf6-19c6e5fb3182
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f1e8df5be24e8773a660a4d0208b27a2f585e32
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730540"
---
# <a name="the-lightweight-client-side-handler"></a>Gestionnaire de Client-Side léger

Les gestionnaires légers côté client vous permettent de créer des gestionnaires généraux côté client de toutes tailles, pour vous aider à effectuer n’importe quel type de tâche standard. En tant que gestionnaires, ceux-ci sont utilisables par plusieurs clients. Ils diffèrent des gestionnaires OLE en ce qu’ils ne peuvent pas être créés avant le lancement du serveur, et leur durée de vie est liée à celle du gestionnaire proxy, ce qui évite une condition de concurrence potentielle dans laquelle le gestionnaire pourrait autrement être libéré prématurément.

Le gestionnaire proxy est l’objet créé par le système qui implémente l’interface [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) . Si vous utilisez le marshaling standard, le système le crée pour vous lorsque vous appelez [**CoGetStandardMarshal**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstandardmarshal) (ou [**CoGetStdMarshalEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex), pour créer un marshaleur agrégé pour les gestionnaires légers) et implémente également les interfaces [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) et [**IMultiQI**](/windows/win32/api/objidlbase/nn-objidlbase-imultiqi) sur l’objet. Côté serveur, il existe un objet système correspondant qui implémente également **IMarshal**. Ces objets gèrent le marshaling pour vous en toute transparence.

Il existe deux types généraux de gestionnaires que vous pouvez implémenter :

-   Gestionnaire qui exécute un service qui ne requiert aucune donnée supplémentaire du serveur
-   Gestionnaire qui utilise des données supplémentaires à partir du serveur

Voici quelques-unes des utilisations possibles des données supplémentaires dans le flux fourni par le serveur :

-   Données statiques du serveur. Quelle que soit l’interface particulière en cours de marshaling, le serveur écrit les mêmes données dans le flux.
-   Données par interface à partir du serveur. En fonction de l’interface particulière en cours de marshaling, le serveur peut écrire des données différentes dans le flux.
-   Assistances par interface. Les composants COM par interface sont agrégés dans le gestionnaire client et délèguent au proxy standard. Par exemple, pour améliorer les performances du réseau, un composant COM pour [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) peut effectuer la mise en cache côté client des données, la lecture anticipée, l’écriture-behind, le verrouillage de l’opération, etc.
-   Version réseau d’une interface. La version réseau de l’interface est différente de l’interface exposée par le client et le code d’application serveur. Il est possible, par exemple, de multiplexer les interfaces exposées IA et IB sur la même interface réseau INetAB, comme le fait le gestionnaire de serveur d’incorporation. Par exemple, il est possible de convertir une interface de transfert de données en une interface réseau qui utilise des canaux pour un transfert de données efficace.

Les clients de niveau inférieure peuvent ne pas avoir la possibilité de démarshaler des interfaces qui ont des gestionnaires personnalisés, pour deux raisons : tout d’abord, ils peuvent ne pas comprendre le CLSID utilisé dans le paquet marshalé personnalisé lorsque le gestionnaire de serveur est agrégé et que l’objet souhaite un gestionnaire. Deuxièmement, le code du gestionnaire ne peut même pas s’exécuter côté client s’il requiert de nouvelles fonctionnalités de COM pour créer le marshaleur standard agrégé et pour effectuer des appels [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) distants.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Le gestionnaire OLE](the-ole-handler.md)
</dt> </dl>

 

 