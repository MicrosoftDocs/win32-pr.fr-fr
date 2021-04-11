---
title: Développement d’applications Windows RPC
description: Lorsque vous installez le kit de développement logiciel (SDK) de la plateforme, l’environnement de développement RPC, les bibliothèques d’exécution et les outils suivants sont installés automatiquement
ms.assetid: d5da3bca-5251-4ba4-b873-0817fe0f298d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b418358649d0cf7205b9a3bde236cf66d3ce81e0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031747"
---
# <a name="developing-rpc-windows-applications"></a>Développement d’applications Windows RPC

Lorsque vous installez le kit de développement logiciel (SDK) de la plateforme, l’environnement de développement RPC suivant, les bibliothèques Runtime et les outils sont automatiquement installés :

-   En-tête du langage C/C++ (. H)
-   Fichiers de bibliothèque d’importation RPC (. lib)
-   Exemples de programmes
-   Fichiers d’aide de référence RPC
-   Utilitaire **uuidgen**

Lorsque vous installez Windows, les éléments suivants sont installés :

-   Dll Runtime RPC
-   Microsoft Locator (non pris en charge sur Windows Vista et versions ultérieures)
-   Services de mappage de point de terminaison RPC

Bibliothèques d’importation RPC suivantes.



| Importer la bibliothèque | Description                |
|----------------|----------------------------|
| Rpcns4. lib     | Fonctions Name-Service     |
| Rpcrt4. lib     | Fonctions runtime Windows |



 

> [!Note]  
> Rpcns4. lib est obsolète et n’est plus pris en charge.

 

Les bibliothèques RPC suivantes sont incluses pour la prise en charge de niveau de service.



| Bibliothèque de liens dynamiques | Description                 | Plate-forme                           |
|----------------------|-----------------------------|------------------------------------|
| Rpcltc1.dll          | Transport du canal nommé du client | Windows NT, Windows 98, Windows 95 |
| Rpclts1.dll          | Transport de canaux nommés du serveur | Windows NT, Windows 98, Windows 95 |
| Rpcltc3.dll          | Transport TCP/IP du client     | Windows NT, Windows 98, Windows 95 |
| Rpclts3.dll          | Transport TCP/IP du serveur     | Windows NT, Windows 98, Windows 95 |
| Rpcltc5.dll          | Transport NetBIOS du client    | Windows NT, Windows 98, Windows 95 |
| Rpclts5.dll          | Transport NetBIOS du serveur    | Windows NT, Windows 98, Windows 95 |
| Rpcltc6.dll          | Transport SPX client        | Windows NT, Windows 98, Windows 95 |
| Rpclts6.dll          | Transport du serveur SPX        | Windows NT, Windows 98, Windows 95 |
| Rpcdgc6.dll          | Transport IPX du client        | Windows NT                         |
| Rpcdgs6.dll          | Transport IPX du serveur        | Windows NT                         |
| Rpcdgc3.dll          | Transport UDP du client        | Windows NT                         |
| Rpcdgs3.dll          | Transport UDP du serveur        | Windows NT                         |



 

Vous aurez également besoin du compilateur Microsoft Interface Definition Language (MIDL). Pour plus d’informations, consultez [utilisation du compilateur MIDL](/windows/desktop/Midl/using-the-midl-compiler-2).

 

 