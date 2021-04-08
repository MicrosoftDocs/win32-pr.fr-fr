---
description: Les fournisseurs de paquets réseau (NPPs) exposent les interfaces IDelaydC, IESP, IRTC et IStats.
ms.assetid: 269b26f5-b794-4920-98da-505eda83c990
title: Sélection d’une interface NPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8dba919302190e1fd89c859f61fca14aaf7d6e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864058"
---
# <a name="selecting-an-npp-interface"></a>Sélection d’une interface NPP

Les fournisseurs de paquets réseau (NPPs) exposent les interfaces [**IDelaydC**](idelaydc.md), [**IESP**](iesp.md), [**IRTC**](irtc.md)et [**IStats**](istats.md) . Chacune de ces interfaces fournit des méthodes similaires pour connecter le NPP au réseau, capturer le trafic réseau et collecter des informations statistiques sur les données capturées. Pour choisir l’interface à utiliser, reportez-vous au tableau suivant.

> [!Note]  
> Lorsque vous connectez un NPP au réseau avec l’une de ces interfaces, vous pouvez utiliser uniquement les méthodes fournies par cette interface. Par exemple, si vous vous connectez au réseau à l’aide de l’interface [**IRTC**](irtc.md) , puis que vous essayez de démarrer une capture avec [**IDelaydC**](idelaydc.md), votre appel pour démarrer la capture échoue et un code d’erreur est renvoyé.

 



| Interface                    | Quand l’utiliser                                                                                                                                                                                                                                                                                                                                     |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDelaydC**](idelaydc.md) | Utilisez pour capturer le trafic réseau et le stocker dans un fichier de capture. Cette interface est utilisée par l’interface utilisateur Moniteur réseau et d’autres applications NPP, qui requièrent le stockage des informations réseau capturées.<br/>                                                                                                                                      |
| [**IESP**](iesp.md)         | Utilisé pour fournir des statistiques améliorées dans un format de fichier ESP spécial. Cette interface est utilisée par les applications NPP qui nécessitent les statistiques améliorées fournies par le format ESP.<br/>                                                                                                                                                        |
| [**IRTC**](irtc.md)         | Utilisez pour capturer le trafic réseau en temps réel et déclencher des événements lorsqu’ils se produisent. Cette interface est utilisée par les applications NPP qui requièrent des captures au moment de l’exécution. Notez que cette interface ne fournit pas les statistiques fournies par les autres interfaces NPP, pas plus qu’elle ne vous permet d’insérer des frames dans le trafic réseau capturé.<br/> |
| [**IStats**](istats.md)     | Utilisez pour récupérer des statistiques de capture, mais pas les frames capturés.                                                                                                                                                                                                                                                                                 |



 

 

 




