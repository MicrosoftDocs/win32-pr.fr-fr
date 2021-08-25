---
description: Lorsqu’une application compatible SOAP a été exportée à partir d’un serveur en mode proxy, les clients qui l’importent peuvent accéder automatiquement aux méthodes des composants qu’elle contient, à distance, en tant que services Web proposés par le serveur en mode d’objet activé par le client (CAO). Cela vous permet de déployer très facilement les fonctionnalités d’une application COM+ sur un réseau sous la forme d’un service Web XML.
ms.assetid: 7f4783f7-4f53-4f0b-bb64-ae7903097d6c
title: Importation d’une application SOAP-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a41a60c2b5ca69197582a684920e9e935f28631779bc632810049f1a7d03945
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858919"
---
# <a name="importing-a-soap-enabled-application"></a>Importation d’une application SOAP-Enabled

Lorsqu’une application compatible SOAP a été [exportée](exporting-a-soap-enabled-application.md) à partir d’un serveur en mode proxy, les clients qui l’importent peuvent accéder automatiquement aux méthodes des composants qu’elle contient, à distance, en tant que services Web proposés par le serveur en mode d’objet activé par le client (CAO). Cela vous permet de déployer très facilement les fonctionnalités d’une application COM+ sur un réseau sous la forme d’un service Web XML.

Lorsque les composants d’une application importés de cette façon sont utilisés sur le client, ils ne s’exécutent pas sur le client, mais sont accessibles à distance à l’aide du service Web XML fourni par le serveur à partir duquel l’application a été exportée. Pour plus d’informations sur l’utilisation des composants d’une application importée de cette manière, consultez [accès aux services Web XML en mode CAO](accessing-xml-web-services-in-cao-mode.md).

## <a name="component-services-administrative-tool"></a>Outil d’administration Services de composants

Pour importer une application compatible SOAP dans un client, procédez comme suit :

1.  Dans l’arborescence de la console de l’outil d’administration Services de composants, sous **services de composants**, ouvrez le dossier associé à l’ordinateur client sur lequel vous souhaitez installer l’application.

2.  Cliquez avec le bouton droit sur le dossier **applications com+** du client, puis choisissez **nouveau**. L' **Assistant Installation de l’application com+** s’affiche.

3.  Dans l' **Assistant Installation de l’application com+**, cliquez sur **installer une ou plusieurs applications prédéfinies**.

4.  Parcourez le réseau pour localiser ou spécifier le chemin d’accès réseau du fichier MSI sur le serveur à partir duquel vous souhaitez installer l’application.

## <a name="visual-basic"></a>Visual Basic

Non applicable.

## <a name="cc"></a>C/C++

Non applicable.

## <a name="remarks"></a>Remarques

Les composants COM sont identifiés par un GUID, qui change si les composants sont recompilés. Si un composant COM configuré qui est exposé en tant que service Web XML est recompilé, les applications clientes qui l’utilisent s’arrêteront. Par conséquent, lorsqu’un composant qui est exposé en tant que service Web XML est recompilé, les clients doivent réimporter les applications qui utilisent le composant.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vue d’ensemble du service SOAP COM+](com--soap-service-overview.md)
</dt> <dt>

[Création de services Web XML](creating-xml-web-services.md)
</dt> <dt>

[Exportation d’une application SOAP-Enabled](exporting-a-soap-enabled-application.md)
</dt> </dl>

 

 



