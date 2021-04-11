---
title: Élément instrumentationManifest
description: Nœud racine du manifeste.
ms.assetid: cb7b5201-be11-48f9-bcca-4606904f0c1d
keywords:
- EventLog, élément instrumentationManifest
topic_type:
- apiref
api_name:
- instrumentationManifest
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c15092d7a7eafd625e9c2026965af053d38fe4b9
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "104211335"
---
# <a name="instrumentationmanifest-element"></a><span data-ttu-id="c0513-104">Élément instrumentationManifest</span><span class="sxs-lookup"><span data-stu-id="c0513-104">instrumentationManifest Element</span></span>

<span data-ttu-id="c0513-105">Nœud racine du manifeste.</span><span class="sxs-lookup"><span data-stu-id="c0513-105">The root node of the manifest.</span></span>

``` syntax
<xs:element name="instrumentationManifest">
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="InstrumentationManifestType"
            >
                <xs:choice
                    maxOccurs="3"
                >
                    <xs:choice>
                        <xs:element name="metadata"
                            type="MetadataType"
                         />
                        <xs:element name="instrumentation"
                            type="InstrumentationType"
                         />
                    </xs:choice>
                    <xs:element name="localization"
                        type="LocalizationType"
                     />
                    <xs:any
                        processContents="lax"
                        minOccurs="0"
                        maxOccurs="unbounded"
                        namespace="##other"
                     />
                </xs:choice>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="c0513-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c0513-106">Child elements</span></span>



| <span data-ttu-id="c0513-107">Élément</span><span class="sxs-lookup"><span data-stu-id="c0513-107">Element</span></span>                                                                                        | <span data-ttu-id="c0513-108">Type</span><span class="sxs-lookup"><span data-stu-id="c0513-108">Type</span></span>                                                                               | <span data-ttu-id="c0513-109">Description</span><span class="sxs-lookup"><span data-stu-id="c0513-109">Description</span></span>                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c0513-110">**Instrumentation**</span><span class="sxs-lookup"><span data-stu-id="c0513-110">**instrumentation**</span></span>](eventmanifestschema-instrumentation-instrumentationmanifest-element.md) | [<span data-ttu-id="c0513-111">**InstrumentationType**</span><span class="sxs-lookup"><span data-stu-id="c0513-111">**InstrumentationType**</span></span>](eventmanifestschema-instrumentationtype-complextype.md) | <span data-ttu-id="c0513-112">Cette section définit un ou plusieurs fournisseurs d’événements et les événements qu’ils consignent.</span><span class="sxs-lookup"><span data-stu-id="c0513-112">This section defines one or more event providers and the events that they log.</span></span><br/>                                                                                                                                                                                                                     |
| [<span data-ttu-id="c0513-113">**localiz**</span><span class="sxs-lookup"><span data-stu-id="c0513-113">**localization**</span></span>](eventmanifestschema-localization-instrumentationmanifest-element.md)       | [<span data-ttu-id="c0513-114">**LocalizationType**</span><span class="sxs-lookup"><span data-stu-id="c0513-114">**LocalizationType**</span></span>](eventmanifestschema-localizationtype-complextype.md)       | <span data-ttu-id="c0513-115">Cette section définit les chaînes de message localisées que les consommateurs utilisent pour l’affichage.</span><span class="sxs-lookup"><span data-stu-id="c0513-115">This section defines the localized message strings that consumers use for display.</span></span> <span data-ttu-id="c0513-116">Par exemple, cette section contient la chaîne de message localisée pour le nom de votre fournisseur, les événements que vous définissez et les attributs d’événement que vous définissez, tels que les canaux, les tâches et les OpCodes.</span><span class="sxs-lookup"><span data-stu-id="c0513-116">For example, this section would contain the localized message string for the name of your provider, the events that you define, and any event attributes that you define, such as channels, tasks, and opcodes.</span></span><br/> |
| [<span data-ttu-id="c0513-117">**Metadata**</span><span class="sxs-lookup"><span data-stu-id="c0513-117">**metadata**</span></span>](eventmanifestschema-metadata-instrumentationmanifest-element.md)               | [<span data-ttu-id="c0513-118">**MetadataType**</span><span class="sxs-lookup"><span data-stu-id="c0513-118">**MetadataType**</span></span>](eventmanifestschema-metadatatype-complextype.md)               | <span data-ttu-id="c0513-119">Cette section définit les types de métadonnées que d’autres manifestes peuvent utiliser.</span><span class="sxs-lookup"><span data-stu-id="c0513-119">This section defines metadata types that other manifests can use.</span></span> <span data-ttu-id="c0513-120">Pour obtenir un exemple, consultez le fichier Winmeta.xml inclus dans le \\ dossier include du SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="c0513-120">For an example, see the Winmeta.xml file included in the \\Include folder of the Windows SDK.</span></span><br/>                                                                                                                                    |



## <a name="remarks"></a><span data-ttu-id="c0513-121">Notes</span><span class="sxs-lookup"><span data-stu-id="c0513-121">Remarks</span></span>

<span data-ttu-id="c0513-122">L’élément **instrumentationManifest** doit contenir les espaces de noms suivants :</span><span class="sxs-lookup"><span data-stu-id="c0513-122">The **instrumentationManifest** element must contain the following namespaces:</span></span>

<dl> <span data-ttu-id="c0513-123">xmlns = " https://schemas.microsoft.com/win/2004/08/events "</span><span class="sxs-lookup"><span data-stu-id="c0513-123">xmlns="https://schemas.microsoft.com/win/2004/08/events"</span></span>  
<span data-ttu-id="c0513-124">xmlns : Win = " https://manifests.microsoft.com/win/2004/08/windows/events "</span><span class="sxs-lookup"><span data-stu-id="c0513-124">xmlns:win="https://manifests.microsoft.com/win/2004/08/windows/events"</span></span>  
<span data-ttu-id="c0513-125">xmlns : XS = " https://www.w3.org/2001/XMLSchema "</span><span class="sxs-lookup"><span data-stu-id="c0513-125">xmlns:xs="https://www.w3.org/2001/XMLSchema"</span></span>  
</dl>

<span data-ttu-id="c0513-126">Un manifeste doit contenir une section instrumentation et une section localization.</span><span class="sxs-lookup"><span data-stu-id="c0513-126">A manifest must contain an instrumentation section and a localization section.</span></span> <span data-ttu-id="c0513-127">La section de métadonnées et la section d’instrumentation s’excluent mutuellement (vous ne pouvez pas définir les deux dans le même manifeste).</span><span class="sxs-lookup"><span data-stu-id="c0513-127">The instrumentation section and metadata section are mutually exclusive (you cannot define both in the same manifest).</span></span> <span data-ttu-id="c0513-128">Bien que vous puissiez créer un manifeste qui contient une section de métadonnées, le service ne l’utilise pas. les seules métadonnées reconnues par le service sont les métadonnées trouvées dans le fichier Winmeta.xml.</span><span class="sxs-lookup"><span data-stu-id="c0513-128">Although you can create a manifest that contains a metadata section, the service will not use it; the only metadata that the service recognizes is the metadata found in the Winmeta.xml file.</span></span>

## <a name="examples"></a><span data-ttu-id="c0513-129">Exemples</span><span class="sxs-lookup"><span data-stu-id="c0513-129">Examples</span></span>

<span data-ttu-id="c0513-130">L’exemple suivant illustre la structure d’un manifeste d’instrumentation entièrement défini.</span><span class="sxs-lookup"><span data-stu-id="c0513-130">The following example shows the skeleton of a fully defined instrumentation manifest.</span></span>


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="https://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="https://www.w3.org/2001/XMLSchema"    
    >

    <instrumentation>
        <events>
            <provider ...>
                <channels>
                    <importChanel .../>
                    <channel .../>
                </channels>
                <levels>
                <level .../>
                </levels>
                <tasks>
                    <task .../>
                </tasks>
                <opcodes>
                    <opcode .../>
                </opcodes>
                <keywords>
                    <keyword .../>
                </keywords>
                <filters>
                    <filter .../>
                </filters>
                <maps>
                    <valueMap ...>
                        <map .../>
                    </valueMap>
                    <bitMap ...>
                        <map .../>
                    </bitMap>
                </maps>
                <namedQueries>
                    <patternMap ...>
                        <map .../>
                    </patternMap>  
                </namedQueries>
                <templates>
                    <template ...>
                        <data .../>
                        <UserData>
                            <!-- valid XML fragment -->
                        </UserData>
                    </template>
                </templates>
                <events>
                    <event .../>
                </events>
            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources ...>
            <stringTable>
                <string .../>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```



## <a name="requirements"></a><span data-ttu-id="c0513-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0513-131">Requirements</span></span>



| <span data-ttu-id="c0513-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c0513-132">Requirement</span></span> | <span data-ttu-id="c0513-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="c0513-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c0513-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c0513-134">Minimum supported client</span></span><br/> | <span data-ttu-id="c0513-135">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c0513-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c0513-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c0513-136">Minimum supported server</span></span><br/> | <span data-ttu-id="c0513-137">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c0513-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





