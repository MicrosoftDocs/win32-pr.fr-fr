---
description: Les fournisseurs de paquets réseau (NPPs) sont des composants système Moniteur réseau qui collectent le trafic réseau (trames) à partir du réseau et les transmettent à l’interface utilisateur Moniteur réseau, ainsi qu’aux applications NPP.
ms.assetid: c966cd00-5cab-4fcf-ad8e-b6c4ffb0e977
title: Fournisseurs de paquets réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8257a62e4f8b0a8434143b2fecba04d9a66c9fb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194631"
---
# <a name="network-packet-providers"></a>Fournisseurs de paquets réseau

Les fournisseurs de paquets réseau (NPPs) sont des composants système Moniteur réseau qui collectent le trafic réseau (trames) à partir du réseau et les transmettent à l’interface utilisateur Moniteur réseau, ainsi qu’aux [*applications NPP*](n.md).

L’illustration suivante montre deux NPPs : le NPP NDIS fourni par Moniteur réseau et un NPP personnalisé.

![NDIS NPP fourni par le moniteur réseau et un NPP personnalisé](images/npp.png)

Le NPP NDIS fourni par Moniteur réseau est Ndisnpp.dll. Ce NPP utilise le pilote de système de Moniteur réseau (Nmnt.sys) pour récupérer les trames collectées à partir du réseau et plusieurs interfaces COM (appelées interfaces NPP) pour transmettre les frames à l’interface utilisateur Moniteur réseau, et les applications NPP, où elles peuvent être affichées et analysées.

Ndisnpp.dll se connecte à la couche [*NDIS*](n.md) pour obtenir son trafic réseau. (Les NPPs personnalisées peuvent contourner la couche NDIS et communiquer directement avec le matériel de mise en réseau.) Sachez que, même si un NPP utilise NDIS, NPPs peut se connecter à n’importe quel nombre de cartes réseau et que tous les NPPs doivent prendre en charge les mêmes interfaces NPP.

Pour qu’une application puisse commencer à capturer des données, elle doit :

-   Sélectionnez la carte d’interface réseau (NIC) qui connectera le NPP au réseau.
-   Sélectionnez l’interface NPP qui sera utilisée pour capturer les trames réseau.
-   Utilisez l’interface sélectionnée pour vous connecter à la carte réseau.

Pour plus d’informations sur l’énumération et la sélection d’une carte d’interface réseau, consultez [sélection d’une carte d’interface réseau](selecting-a-network-interface-card.md).

Pour plus d’informations sur les interfaces COM exposées par NPPs, consultez [sélection d’une interface NPP](selecting-an-npp-interface.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IDelaydC**](idelaydc.md)
</dt> <dt>

[**IESP**](iesp.md)
</dt> <dt>

[**IRTC**](irtc.md)
</dt> <dt>

[**IStats**](istats.md)
</dt> </dl>

 

 



