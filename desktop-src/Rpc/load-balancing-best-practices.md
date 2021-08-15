---
title: Meilleures pratiques relatives à l’équilibrage de charge
description: Meilleures pratiques relatives à l’équilibrage de charge
ms.assetid: 260cf8dd-13b8-4b46-93a6-5333e794c0d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16fe4af9dffe758c89d1a494d4cc2597e057c563ca8c85db87d789ae91b89698
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928594"
---
# <a name="load-balancing-best-practices"></a>Meilleures pratiques relatives à l’équilibrage de charge

Plusieurs meilleures pratiques doivent être suivies lors de la configuration et de la configuration de l’équilibrage de charge RPC.

Tout d’abord, la sécurité doit être définie sur les appels entrants et sortants. Cela signifie que les deux clés de Registre facultatives de type [NoSecurity](configuring-load-balancing.md) ne doivent pas être présentes ou doivent être définies sur zéro.

Deuxièmement, vous devez être attentif à la solution d’équilibrage de charge frontale utilisée conjointement avec la solution d’équilibrage de charge RPC. Par exemple, si l’équilibreur de charge du serveur frontal utilise l’équilibrage de charge de tourniquet (Round Robin) simple, un nombre impair de serveurs doit exister dans la batterie de serveurs. Cela permet d’atténuer le risque que toutes les connexions soient transférées et donc traitées par le ou les mêmes serveurs.

Pour des risques de sécurité, il est généralement préférable d’avoir un pare-feu qui contrôle l’accès aux serveurs proxy RPC. Si une solution de pare-feu basée sur les ports est utilisée, les points de terminaison RPC doivent être statiques afin de limiter le nombre de ports ouverts dans le pare-feu. sur Windows Server 2008 et versions ultérieures de Windows, RPC fournit un mécanisme pour assigner un port statique aux points de terminaison dynamiques. Cela est possible via les commandes de pare-feu netsh RPC. Un exemple de jeu de commandes permettant de définir l’interface LBS sur le port statique 3010 est le suivant :

``` syntax
netsh rpc filter add rule layer=ep_add actiontype=permit

netsh rpc filter add condition field=process_with_if_uuid matchtype=equal data=
3357951c-a1d1-47db-a278-ab945d063d03

netsh rpc filter add condition field=protocol matchtype=equal data=ncacn_ip_tcp

netsh rpc filter add condition field=ep_value matchtype=equal data=w3010

netsh rpc filter add filter
```

La commande RPC netsh peut être utilisée pour définir un point de terminaison statique pour toute interface dynamique ou statique. Cela est utile lors de la restriction de l’accès à une machine exécutant une solution de pare-feu basée sur des ports. si la solution de pare-feu Windows est utilisée, l’interface RPC peut être bloquée ou activée sans avoir à l’assigner à un port spécifique. Pour plus d’informations, consultez les informations de référence sur les [commandes de pare-feu netsh RPC](/previous-versions/windows/it-pro/windows-server-2003/cc784909(v=ws.10)).

 

 