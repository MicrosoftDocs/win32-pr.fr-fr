---
description: Deux exemples WSDAPI sont inclus avec le SDK Windows pour Windows Server 2008.
ms.assetid: 156b79ef-1f05-4ef1-9df9-81fe81c73ca7
title: Exemples WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed088c43f9617da062d5e4fb4f0343f74e3bcbc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754957"
---
# <a name="wsdapi-samples"></a>Exemples WSDAPI

Deux exemples WSDAPI sont inclus avec le SDK Windows pour Windows Server 2008. Le code source des exemples se trouve dans <Windows SDK Install Folder> \\ Samples \\ Web \\ wsdapi. Cette version du kit de développement logiciel (SDK) est disponible à partir du [Centre de téléchargement](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf). Les exemples ne sont pas disponibles dans le kit de développement logiciel (SDK) Windows Vista.

L’exemple Stock Quote (situé dans <Windows SDK Install Folder> \\ Samples \\ Web \\ wsdapi \\ StockQuote) illustre un service avec des fonctionnalités de messagerie de base. L’exemple de service de fichiers (situé dans <Windows SDK Install Folder> \\ Samples \\ Web \\ wsdapi \\ FileService) illustre un service avec des fonctionnalités avancées, telles que la messagerie asynchrone, les pièces jointes et les événements.

Les deux exemples incluent les types de fichiers suivants.

-   Fichiers WSDL qui contiennent les descriptions de service.
-   [Fichiers de configuration WsdCodeGen](wsdcodegen-configuration-file.md) utilisés pour générer le code wsdapi.
-   Fichiers sources et d’en-tête C++ générés.
-   Fichiers d’implémentation du client et du service.
-   Fichiers projet et solution Visual Studio.

Les deux exemples implémentent les hôtes d’appareils ([**IWSDDeviceHost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost)), les proxys d’appareil ([**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy)) et les proxys de service ([**IWSDServiceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdserviceproxy)). En outre, l’exemple de service de fichiers montre l’utilisation de la messagerie asynchrone ([**IWSDAsyncCallback**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdasynccallback), [**IWSDAsyncResult**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdasyncresult)), des pièces jointes ([**IWSDInboundAttachment**](/windows/desktop/api/WsdAttachment/nn-wsdattachment-iwsdinboundattachment), [**IWSDOutboundAttachment**](/windows/desktop/api/WsdAttachment/nn-wsdattachment-iwsdoutboundattachment)) et des événements.

Les fichiers FileServiceContract. vcproj et StockQuoteContract. vcproj inclus avec les exemples appellent [WsdCodeGen](web-services-for-devices-code-generator.md) pour générer des fichiers d’en-tête C++ et des fichiers sources à partir du fichier WSDL spécifié dans le fichier de configuration WsdCodeGen. Cela signifie que si l’exemple de fichier de configuration WSDL ou WsdCodeGen est modifié et que l’exemple de projet est régénéré, WsdCodeGen génère automatiquement de nouveaux fichiers d’en-tête et sources qui reflètent les modifications. Il s’agit de la méthode recommandée pour générer des applications WSDAPI. WsdCodeGen est généralement appelé à partir de la ligne de commande. Ouvrez le \* fichier. vcproj approprié pour afficher les exemples d’appels de ligne de commande WsdCodeGen.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Développement d’applications WSD sur Windows](wsd-application-development-on-windows.md)
</dt> </dl>

 

 



