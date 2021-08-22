---
description: Les fournisseurs de paquets réseau (NPPs) fournissent des interfaces COM qui sont appelées par les applications NPP et Moniteur réseau.
ms.assetid: 101ce722-3101-4f50-b492-dad8b68a7aaf
title: Interfaces NPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22fc38bd5db91354c81f88d9f0fe0a6ad23ce3ccb3ecd4a08c4b6335e25ddd33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676979"
---
# <a name="npp-interfaces"></a>Interfaces NPP

Les fournisseurs de paquets réseau (NPPs) fournissent des interfaces COM qui sont appelées par les applications NPP et Moniteur réseau. Lorsque vous appelez [CreateNPPInterface](createnppinterface.md), rappelez-vous que chaque npp est représenté sous la forme d’un objet com in-process unique. Les applications peuvent instancier un nombre quelconque d’objets NPP. Toutefois, chaque objet instancié doit utiliser un et une seule des cinq interfaces NPP.

Notez également que différentes interfaces NPP fournissent des données réseau sous différentes formes. Par exemple, Moniteur réseau utilise l’interface **IDelaydC** pour capturer le trafic réseau et l’enregistrer dans un fichier de capture. tandis que les analyses utilisent l’interface **IRTC** pour capturer le trafic réseau en temps réel. Le tableau suivant décrit Moniteur réseau interfaces NPP.



| Interface                | Description                                                                                                                                                         |
|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IDelaydC](idelaydc.md) | Capture le trafic réseau qui est stocké dans un fichier de capture. Cette interface est utilisée par les applications Moniteur réseau et NPP.                                          |
| [IESP](iesp.md)         | Capture le trafic réseau qui est stocké dans un fichier de capture et fournit des statistiques améliorées dans un format de fichier ESP spécial. Cette interface est utilisée par les applications NPP |
| [IRTC](irtc.md)         | Capture le trafic réseau en temps réel et déclenche des événements lorsqu’ils se produisent. Cette interface est utilisée par les [*analyses*](m.md) et les applications NPP.     |
| [IStats](istats.md)     | Récupère des statistiques sous forme de données brutes plutôt que de frames. Cette interface est utilisée par les applications NPP telles que [*Perfmon*](p.md).                     |



 

 

 



