---
title: Type complexe EventsType
description: Contient une liste de fournisseurs définis dans le manifeste. | Type complexe EventsType
ms.assetid: 43f9f577-eae0-45c5-aaf0-5a6df28d3b79
keywords:
- EventsType type complexe EventLog
topic_type:
- apiref
api_name:
- EventsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 36500aa037c8e33a48b4f9dd6e38e46eaac58da2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106531282"
---
# <a name="eventstype-complex-type"></a><span data-ttu-id="7b34b-105">Type complexe EventsType</span><span class="sxs-lookup"><span data-stu-id="7b34b-105">EventsType Complex Type</span></span>

<span data-ttu-id="7b34b-106">Contient une liste de fournisseurs définis dans le manifeste.</span><span class="sxs-lookup"><span data-stu-id="7b34b-106">Contains a list of providers that are defined in the manifest.</span></span>

``` syntax
<xs:complexType name="EventsType">
    <xs:choice
        maxOccurs="unbounded"
    >
        <xs:element name="provider"
            type="ProviderType"
            maxOccurs="unbounded"
         />
        <xs:element name="messageTable"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:sequence>
                    <xs:element name="message"
                        minOccurs="0"
                        maxOccurs="unbounded"
                    >
                        <xs:complexType>
                            <xs:attribute name="value"
                                type="UInt32Type"
                                use="required"
                             />
                            <xs:attribute name="mid"
                                type="xs:string"
                                use="optional"
                             />
                            <xs:attribute name="message"
                                type="strTableRef"
                                use="required"
                             />
                            <xs:attribute name="symbol"
                                type="CSymbolType"
                                use="optional"
                             />
                        </xs:complexType>
                    </xs:element>
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:choice>
    <xs:anyAttribute
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="7b34b-107">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="7b34b-107">Child elements</span></span>

| <span data-ttu-id="7b34b-108">Élément</span><span class="sxs-lookup"><span data-stu-id="7b34b-108">Element</span></span> | <span data-ttu-id="7b34b-109">Type</span><span class="sxs-lookup"><span data-stu-id="7b34b-109">Type</span></span> | <span data-ttu-id="7b34b-110">Description</span><span class="sxs-lookup"><span data-stu-id="7b34b-110">Description</span></span> |
|---------|------|-------------|
| <span data-ttu-id="7b34b-111">message</span><span class="sxs-lookup"><span data-stu-id="7b34b-111">message</span></span> |      | <span data-ttu-id="7b34b-112">Définit une chaîne de message.</span><span class="sxs-lookup"><span data-stu-id="7b34b-112">Defines a message string.</span></span> |
| <span data-ttu-id="7b34b-113">messageTable</span><span class="sxs-lookup"><span data-stu-id="7b34b-113">messageTable</span></span> | | <span data-ttu-id="7b34b-114">Définit une liste de chaînes de message.</span><span class="sxs-lookup"><span data-stu-id="7b34b-114">Defines a list of message strings.</span></span> <span data-ttu-id="7b34b-115">Vous ne devez pas être obligé d’utiliser une table de messages, sauf dans les cas suivants où vous devez définir une table de messages pour assigner explicitement des numéros de ressource aux chaînes de message.</span><span class="sxs-lookup"><span data-stu-id="7b34b-115">You should not have to use a message table except in the following cases where you must define a message table to explicitly assign resource numbers to message strings.</span></span> <ul><li><span data-ttu-id="7b34b-116">Vous effectuez une migration à partir d’un fichier texte de message (. MC) vers un manifeste, mais vous écrivez toujours des événements sur les canaux de l’application et du système, afin que les consommateurs hérités continuent de consommer les événements.</span><span class="sxs-lookup"><span data-stu-id="7b34b-116">You are migrating from a message text (.mc) file to a manifest but are still writing events to the application and system channels, so that legacy consumers to continue consuming the events.</span></span> <span data-ttu-id="7b34b-117">Pour que cela fonctionne, les identificateurs de ressource pour les chaînes de message définies dans le manifeste doivent être les mêmes que les identificateurs d’événements.</span><span class="sxs-lookup"><span data-stu-id="7b34b-117">To make this work, the resource identifiers for the message strings defined in the manifest must be the same as the event identifiers.</span></span> <span data-ttu-id="7b34b-118">Toutefois, le compilateur de message affecte automatiquement des identificateurs de ressource aux chaînes de message.</span><span class="sxs-lookup"><span data-stu-id="7b34b-118">However, the message compiler automatically assigns resource identifiers to the message strings.</span></span> <span data-ttu-id="7b34b-119">Pour remplacer le compilateur, utilisez la table de messages et affectez à l’attribut value la valeur de l’identificateur d’événement et l’attribut de message pour faire référence à une chaîne dans la table de chaînes de la section localization du manifeste.</span><span class="sxs-lookup"><span data-stu-id="7b34b-119">To override the compiler, use the message table and set the value attribute to the event identifier and the message attribute to refer to a string in the string table in the localization section of the manifest.</span></span></li><li><span data-ttu-id="7b34b-120">Si vous souhaitez identifier plus de 16 fournisseurs, vous devez inclure la table de messages que les fournisseurs dix-septième et sur doivent utiliser pour assigner des valeurs de ressource pour les chaînes de message qu’ils définissent.</span><span class="sxs-lookup"><span data-stu-id="7b34b-120">If you want to identify more than 16 providers, you must include the message table that the seventeenth and on providers must use to assign resource values for the message strings that they define.</span></span> <span data-ttu-id="7b34b-121">Si le fournisseur fait référence à des chaînes de message que les fournisseurs 1 à 16 sont définies, vous n’incluez pas ces chaînes de message dans la table des messages.</span><span class="sxs-lookup"><span data-stu-id="7b34b-121">If the provider references message strings that providers 1 through 16 defined, you do not include those message strings in the message table.</span></span></li></ul>|
| [<span data-ttu-id="7b34b-122">**moteur**</span><span class="sxs-lookup"><span data-stu-id="7b34b-122">**provider**</span></span>](eventmanifestschema-provider-eventstype-element.md) | [<span data-ttu-id="7b34b-123">**ProviderType**</span><span class="sxs-lookup"><span data-stu-id="7b34b-123">**ProviderType**</span></span>](eventmanifestschema-providertype-complextype.md) | <span data-ttu-id="7b34b-124">Liste des fournisseurs que vous souhaitez définir.</span><span class="sxs-lookup"><span data-stu-id="7b34b-124">A list of providers that you want to define.</span></span> |

## <a name="attributes"></a><span data-ttu-id="7b34b-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="7b34b-125">Attributes</span></span>

| <span data-ttu-id="7b34b-126">Nom</span><span class="sxs-lookup"><span data-stu-id="7b34b-126">Name</span></span>    | <span data-ttu-id="7b34b-127">Type</span><span class="sxs-lookup"><span data-stu-id="7b34b-127">Type</span></span>                                                             | <span data-ttu-id="7b34b-128">Description</span><span class="sxs-lookup"><span data-stu-id="7b34b-128">Description</span></span>                                                                            |
|---------|------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b34b-129">message</span><span class="sxs-lookup"><span data-stu-id="7b34b-129">message</span></span> | [<span data-ttu-id="7b34b-130">**strTableRef**</span><span class="sxs-lookup"><span data-stu-id="7b34b-130">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="7b34b-131">Référence à la chaîne localisée dans la table de chaînes.</span><span class="sxs-lookup"><span data-stu-id="7b34b-131">A reference to the localized string in the string table.</span></span>                               |
| <span data-ttu-id="7b34b-132">mid</span><span class="sxs-lookup"><span data-stu-id="7b34b-132">mid</span></span>     | <span data-ttu-id="7b34b-133">xs:string</span><span class="sxs-lookup"><span data-stu-id="7b34b-133">xs:string</span></span>                                                        | <span data-ttu-id="7b34b-134">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="7b34b-134">Not used.</span></span>                                                                              |
| <span data-ttu-id="7b34b-135">symbole</span><span class="sxs-lookup"><span data-stu-id="7b34b-135">symbol</span></span>  | [<span data-ttu-id="7b34b-136">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="7b34b-136">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="7b34b-137">Nom symbolique que vous souhaitez que le compilateur de message crée pour cette chaîne de message.</span><span class="sxs-lookup"><span data-stu-id="7b34b-137">The symbolic name that you want the message compiler to create for this message string.</span></span>|
| <span data-ttu-id="7b34b-138">value</span><span class="sxs-lookup"><span data-stu-id="7b34b-138">value</span></span>   | [<span data-ttu-id="7b34b-139">**UInt32Type**</span><span class="sxs-lookup"><span data-stu-id="7b34b-139">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="7b34b-140">Nombre à utiliser comme identificateur de message pour ce message.</span><span class="sxs-lookup"><span data-stu-id="7b34b-140">The number to use as the message identifier for this message.</span></span>                          |


## <a name="remarks"></a><span data-ttu-id="7b34b-141">Notes</span><span class="sxs-lookup"><span data-stu-id="7b34b-141">Remarks</span></span>

<span data-ttu-id="7b34b-142">La limite pratique du nombre de fournisseurs que vous pouvez définir dans un manifeste est de 16 fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="7b34b-142">The practical limit of the number of providers that you can define in a manifest is 16 providers.</span></span> <span data-ttu-id="7b34b-143">Si vous spécifiez plus de 16 fournisseurs, vous devez utiliser une table de messages pour assigner explicitement des numéros de ressource aux chaînes de message auxquelles le fournisseur fait référence.</span><span class="sxs-lookup"><span data-stu-id="7b34b-143">If you specify more than 16 providers, you must use a message table to explicitly assign resource numbers to the message strings that the provider references.</span></span> <span data-ttu-id="7b34b-144">Pour plus d’informations, consultez l’élément message ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="7b34b-144">For more details, see the message element above.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b34b-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7b34b-145">Requirements</span></span>

| <span data-ttu-id="7b34b-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7b34b-146">Requirement</span></span> | <span data-ttu-id="7b34b-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="7b34b-147">Value</span></span> |
|--------------------------|-------------------------------------------|
| <span data-ttu-id="7b34b-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b34b-148">Minimum supported client</span></span> | <span data-ttu-id="7b34b-149">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7b34b-149">Windows Vista \[desktop apps only\]</span></span>       |
| <span data-ttu-id="7b34b-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b34b-150">Minimum supported server</span></span> | <span data-ttu-id="7b34b-151">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7b34b-151">Windows Server 2008 \[desktop apps only\]</span></span> |
