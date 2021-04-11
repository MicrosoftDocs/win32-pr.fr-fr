---
description: Cette section décrit la structure de qualité de service (QOS) propre au protocole pour ATM, qui est contenue dans le champ ProviderSpecific de la structure QOS.
ms.assetid: ec7882f7-7197-439a-82a4-ff081505a9d7
title: Extension Winsock ATM QoS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 075c9dcbd8b9148f41d39c99e2118ed638a577ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112990"
---
# <a name="winsock-atm-qos-extension"></a><span data-ttu-id="497b1-103">Extension Winsock ATM QoS</span><span class="sxs-lookup"><span data-stu-id="497b1-103">Winsock ATM QoS Extension</span></span>

<span data-ttu-id="497b1-104">Cette section décrit la structure de qualité de service ([**QoS**](/windows/win32/api/winsock2/ns-winsock2-qos)) propre au protocole pour ATM, qui est contenue dans le champ [providerspecific](/previous-versions/aa374467(v=vs.80)) de la structure **QoS** .</span><span class="sxs-lookup"><span data-stu-id="497b1-104">This section describes the protocol-specific Quality of Service ([**QOS**](/windows/win32/api/winsock2/ns-winsock2-qos)) structure for ATM, which is contained in the [ProviderSpecific](/previous-versions/aa374467(v=vs.80)) field of the **QOS** structure.</span></span> <span data-ttu-id="497b1-105">Notez que l’utilisation de cette structure **QoS** spécifique à ATM est facultative pour les clients Windows Sockets 2 et que le fournisseur de services ATM est requis pour mapper la structure du [**FLOWSPEC**](/windows/win32/api/qos/ns-qos-flowspec) générique aux éléments d’informations Q. 2931 appropriés.</span><span class="sxs-lookup"><span data-stu-id="497b1-105">Note that the use of this ATM-specific **QOS** structure is optional by Windows Sockets 2 clients, and the ATM service provider is required to map the generic [**FLOWSPEC**](/windows/win32/api/qos/ns-qos-flowspec) structure to appropriate Q.2931 information elements.</span></span> <span data-ttu-id="497b1-106">Toutefois, si la structure du **FLOWSPEC** générique et la structure **QoS** propre à la ATM sont spécifiées, la valeur spécifiée dans la structure **QoS** spécifique à ATM doit être prioritaire.</span><span class="sxs-lookup"><span data-stu-id="497b1-106">However, if both the generic **FLOWSPEC** structure and ATM-specific **QOS** structure are specified, the value specified in the ATM-specific **QOS** structure should take precedence should there be any conflicts.</span></span> <span data-ttu-id="497b1-107">Consultez la spécification de l’API Windows Sockets 2, section 2,7 pour plus d’informations sur les dispositions de QoS et la structure **FLOWSPEC** .</span><span class="sxs-lookup"><span data-stu-id="497b1-107">See Windows Sockets 2 API Specification Section 2.7 for more information about QoS provisions and **FLOWSPEC** structure.</span></span>

<span data-ttu-id="497b1-108">La structure [**QoS**](/windows/win32/api/winsock2/ns-winsock2-qos) propre au protocole pour ATM est une concaténation des structures d’élément d’information Q. 2931, qui sont définies dans le texte suivant.</span><span class="sxs-lookup"><span data-stu-id="497b1-108">The protocol-specific [**QOS**](/windows/win32/api/winsock2/ns-winsock2-qos) structure for ATM is a concatenation of Q.2931 information element (IE) structures, which are defined in the following text.</span></span> <span data-ttu-id="497b1-109">Si une application omet un IE qui est imposé par UNI 3. x, le fournisseur de services doit insérer une valeur par défaut raisonnable, en tenant compte des informations contenues dans la structure [**FLOWSPEC**](/windows/win32/api/qos/ns-qos-flowspec) , le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="497b1-109">If an application omits an IE that UNI 3.x mandates, the service provider should insert a reasonable default value, taking the information in the [**FLOWSPEC**](/windows/win32/api/qos/ns-qos-flowspec) structure into account if applicable.</span></span>

<span data-ttu-id="497b1-110">La gestion des objets récurrents est tributaire de l’IE lui-même.</span><span class="sxs-lookup"><span data-stu-id="497b1-110">The handling of repeated IEs is dependent on the IE itself.</span></span> <span data-ttu-id="497b1-111">Si une instance d’Internet Explorer est répétée et qu’il s’agit d’une opération qui peut être répétée en fonction de la spécification UNI du Forum ATM, le fournisseur doit le gérer correctement.</span><span class="sxs-lookup"><span data-stu-id="497b1-111">If an IE is repeated and it is one that is allowed to be repeated per the ATM Forum UNI specification then the provider must handle it properly.</span></span> <span data-ttu-id="497b1-112">Dans ce cas, l’ordre dans la liste détermine l’ordre des préférences, les éléments apparaissant plus tôt dans la liste étant plus préférés.</span><span class="sxs-lookup"><span data-stu-id="497b1-112">In this case, order in the list determines preference order, with elements appearing earlier in the list being more preferred.</span></span> <span data-ttu-id="497b1-113">Si un IE est répété et que cela n’est pas autorisé par la spécification UNI du Forum ATM, le fournisseur peut soit faire échouer la demande à partir du client (option par défaut), soit utiliser le dernier IE de ce type trouvé.</span><span class="sxs-lookup"><span data-stu-id="497b1-113">If an IE is repeated and this is not allowed per ATM Forum UNI specification, the provider may either fail the request from the client (the preferred option) or use the last IE of that type found.</span></span>

<span data-ttu-id="497b1-114">Chaque structure IE individuelle est mise en forme de la manière suivante et identifiée par le champ **IEType** :</span><span class="sxs-lookup"><span data-stu-id="497b1-114">Each individual IE structure is formatted in the following manner and identified by the **IEType** field:</span></span>

``` syntax
typedef struct {
    Q2931_IE_TYPE IEType;
    ULONG         IELength;
    UCHAR         IE[1];
} Q2931_IE;
```

<span data-ttu-id="497b1-115">Les valeurs autorisées pour le champ **IEType** sont définies comme suit :</span><span class="sxs-lookup"><span data-stu-id="497b1-115">Legal values for the **IEType** field are defined as:</span></span>

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

<span data-ttu-id="497b1-116">Le champ **IE** est recouvert par une structure IE spécifique et le champ **IELength** est la longueur totale, en octets, de la structure IE, y compris les champs **IEType** et **IELength** .</span><span class="sxs-lookup"><span data-stu-id="497b1-116">The **IE** field is overlaid by a specific IE structure and the **IELength** field is the total length in bytes of the IE structure including the **IEType** and **IELength** fields.</span></span> <span data-ttu-id="497b1-117">La sémantique et les valeurs autorisées pour chaque élément de ces structures IE sont par spécification ATM UNI 3. x.</span><span class="sxs-lookup"><span data-stu-id="497b1-117">The semantics and legal values for each element of these IE structures are per ATM UNI 3.x specification.</span></span> <span data-ttu-id="497b1-118">\_Le champ SAP \_ absent peut être utilisé pour les éléments qui sont facultatifs pour une structure IE donnée, par spécification ATM Uni 3. x.</span><span class="sxs-lookup"><span data-stu-id="497b1-118">SAP\_FIELD\_ABSENT can be used for those elements that are optional for a given IE structure, per ATM UNI 3.x specification.</span></span>

 

 
