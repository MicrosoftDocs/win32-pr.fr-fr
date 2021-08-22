---
description: Cette section décrit la structure de qualité de service (QOS) propre au protocole pour ATM, qui est contenue dans le champ ProviderSpecific de la structure QOS.
ms.assetid: ec7882f7-7197-439a-82a4-ff081505a9d7
title: Extension Winsock ATM QoS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 422db2df8e4f845086120814f6cf4e6288dcc00c42693eac8da21c466448aaa6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612819"
---
# <a name="winsock-atm-qos-extension"></a>Extension Winsock ATM QoS

Cette section décrit la structure de qualité de service ([**QoS**](/windows/win32/api/winsock2/ns-winsock2-qos)) propre au protocole pour ATM, qui est contenue dans le champ [providerspecific](/previous-versions/aa374467(v=vs.80)) de la structure **QoS** . notez que l’utilisation de cette structure **QOS** spécifique à atm est facultative par Windows les clients sockets 2 et que le fournisseur de services atm est requis pour mapper la structure du [**FLOWSPEC**](/windows/win32/api/qos/ns-qos-flowspec) générique aux éléments d’informations Q. 2931 appropriés. Toutefois, si la structure du **FLOWSPEC** générique et la structure **QoS** propre à la ATM sont spécifiées, la valeur spécifiée dans la structure **QoS** spécifique à ATM doit être prioritaire. pour plus d’informations sur les dispositions de QoS et la structure **FLOWSPEC** , consultez la Section 2,7 de la spécification de l’API Windows sockets 2.

La structure [**QoS**](/windows/win32/api/winsock2/ns-winsock2-qos) propre au protocole pour ATM est une concaténation des structures d’élément d’information Q. 2931, qui sont définies dans le texte suivant. Si une application omet un IE qui est imposé par UNI 3. x, le fournisseur de services doit insérer une valeur par défaut raisonnable, en tenant compte des informations contenues dans la structure [**FLOWSPEC**](/windows/win32/api/qos/ns-qos-flowspec) , le cas échéant.

La gestion des objets récurrents est tributaire de l’IE lui-même. Si une instance d’Internet Explorer est répétée et qu’il s’agit d’une opération qui peut être répétée en fonction de la spécification UNI du Forum ATM, le fournisseur doit le gérer correctement. Dans ce cas, l’ordre dans la liste détermine l’ordre des préférences, les éléments apparaissant plus tôt dans la liste étant plus préférés. Si un IE est répété et que cela n’est pas autorisé par la spécification UNI du Forum ATM, le fournisseur peut soit faire échouer la demande à partir du client (option par défaut), soit utiliser le dernier IE de ce type trouvé.

Chaque structure IE individuelle est mise en forme de la manière suivante et identifiée par le champ **IEType** :

``` syntax
typedef struct {
    Q2931_IE_TYPE IEType;
    ULONG         IELength;
    UCHAR         IE[1];
} Q2931_IE;
```

Les valeurs autorisées pour le champ **IEType** sont définies comme suit :

``` syntax
typedef enum {
    IE_AALParameters,
    IE_TrafficDescriptor,
    IE_BroadbandBearerCapability,
    IE_BHLI,
    IE_BLLI,
    IE_CalledPartyNumber,
    IE_CalledPartySubaddress,
    IE_CallingPartyNumber,
    IE_CallingPartySubaddress,
    IE_Cause,
    IE_QOSClass,
    IE_TransitNetworkSelection,
} Q2931_IE_TYPE;
```

Le champ **IE** est recouvert par une structure IE spécifique et le champ **IELength** est la longueur totale, en octets, de la structure IE, y compris les champs **IEType** et **IELength** . La sémantique et les valeurs autorisées pour chaque élément de ces structures IE sont par spécification ATM UNI 3. x. \_Le champ SAP \_ absent peut être utilisé pour les éléments qui sont facultatifs pour une structure IE donnée, par spécification ATM Uni 3. x.

 

 
