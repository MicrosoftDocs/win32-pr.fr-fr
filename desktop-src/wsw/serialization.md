---
title: Sérialisation
description: La sérialisation est le processus d’écriture de valeurs dans les structures de données C (structs, tableaux et valeurs primitives) en tant qu’élément XML. La désérialisation est le processus inverse.
ms.assetid: aa092156-30ae-4f8a-baa2-450f38a78153
keywords:
- Services Web de sérialisation pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63f986c6cec9a035424aaafe1c51f4dc0d3ee014
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2021
ms.locfileid: "104211198"
---
# <a name="serialization"></a><span data-ttu-id="61563-107">Sérialisation</span><span class="sxs-lookup"><span data-stu-id="61563-107">Serialization</span></span>

<span data-ttu-id="61563-108">La sérialisation est le processus d’écriture de valeurs dans les structures de données C (structs, tableaux et valeurs primitives) en tant qu’élément XML.</span><span class="sxs-lookup"><span data-stu-id="61563-108">Serialization is the process of writing values in C data structures (structs, arrays, and primitive values) as an XML element.</span></span> <span data-ttu-id="61563-109">La désérialisation est le processus inverse.</span><span class="sxs-lookup"><span data-stu-id="61563-109">Deserialization is the reverse process.</span></span>


<span data-ttu-id="61563-110">La sérialisation est le processus d’écriture de valeurs dans les structures de données C (structures, tableaux et valeurs primitives) en tant qu’élément XML.</span><span class="sxs-lookup"><span data-stu-id="61563-110">Serialization is the process of writing values in C data structures (structures, arrays, and primitive values) as an XML element.</span></span> <span data-ttu-id="61563-111">La désérialisation est le processus inverse.</span><span class="sxs-lookup"><span data-stu-id="61563-111">Deserialization is the reverse process.</span></span>

<span data-ttu-id="61563-112">Les deux processus reposent sur une description du mappage entre les structures de données C et XML.</span><span class="sxs-lookup"><span data-stu-id="61563-112">Both processes rely on a description of the mapping between the C data structures and the XML.</span></span>

![Diagramme montrant comment la sérialisation et la désérialisation reposent sur une description du mappage entre les structures de données C et XML.](images/xmlmapping.png)

<span data-ttu-id="61563-114">Pour sérialiser une valeur, l’application appelle [**WsWriteElement**](/windows/desktop/api/WebServices/nf-webservices-wswriteelement), [**WsWriteAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswriteattribute) ou [**WsWriteType**](/windows/desktop/api/WebServices/nf-webservices-wswritetype).</span><span class="sxs-lookup"><span data-stu-id="61563-114">To serialize a value, the application calls [**WsWriteElement**](/windows/desktop/api/WebServices/nf-webservices-wswriteelement), [**WsWriteAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswriteattribute) or [**WsWriteType**](/windows/desktop/api/WebServices/nf-webservices-wswritetype).</span></span>

<span data-ttu-id="61563-115">Pour désérialiser une valeur, l’application appelle [**WsReadElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadelement), [**WsReadAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsreadattribute) ou [**WsReadType**](/windows/desktop/api/WebServices/nf-webservices-wsreadtype).</span><span class="sxs-lookup"><span data-stu-id="61563-115">To deserialize a value, the application calls [**WsReadElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadelement), [**WsReadAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsreadattribute) or [**WsReadType**](/windows/desktop/api/WebServices/nf-webservices-wsreadtype).</span></span>

## <a name="security"></a><span data-ttu-id="61563-116">Sécurité</span><span class="sxs-lookup"><span data-stu-id="61563-116">Security</span></span>

<span data-ttu-id="61563-117">Le [lecteur XML](xml-reader.md) est utilisé dans le processus de désérialisation.</span><span class="sxs-lookup"><span data-stu-id="61563-117">[XML Reader](xml-reader.md) is used in deserialization process.</span></span> <span data-ttu-id="61563-118">Reportez-vous à la section sécurité dans le lecteur XML pour obtenir des informations de sécurité liées à XML.</span><span class="sxs-lookup"><span data-stu-id="61563-118">Refer to the security section in XML Reader for XML related security information.</span></span>

<span data-ttu-id="61563-119">Le désérialiseur continue à désérialiser les données jusqu’à ce qu’il ait terminé de lire l’élément en cours de désérialisation.</span><span class="sxs-lookup"><span data-stu-id="61563-119">The deserializer continues to deserialize data until it has completed reading the element being deserialized.</span></span> <span data-ttu-id="61563-120">Le processus de désérialisation échoue lorsqu’il rencontre un document XML qui n’est pas conforme à la description des données désérialisées.</span><span class="sxs-lookup"><span data-stu-id="61563-120">Deserialization process fails when it encounter any XML document that does not conform to the description of the data being deserialized.</span></span> <span data-ttu-id="61563-121">À ce stade, le lecteur XML utilisé devient non valide et une erreur est retournée.</span><span class="sxs-lookup"><span data-stu-id="61563-121">At that point XML reader being used becomes invalid, and an error is returned.</span></span>

<span data-ttu-id="61563-122">Par défaut, la désérialisation est stricte.</span><span class="sxs-lookup"><span data-stu-id="61563-122">By default deserialization is strict.</span></span> <span data-ttu-id="61563-123">Certaines conditions provoquant l’échec de la désérialisation incluent, sans s’y limiter, les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="61563-123">Some conditions that cause deserialization to fail include but not limited to:</span></span>

-   <span data-ttu-id="61563-124">Éléments attendus manquants</span><span class="sxs-lookup"><span data-stu-id="61563-124">Expected elements is missing</span></span>
-   <span data-ttu-id="61563-125">Des champs d’élément inattendus apparaissent entre les éléments requis</span><span class="sxs-lookup"><span data-stu-id="61563-125">Unexpected element fields appear between required elements</span></span>
-   <span data-ttu-id="61563-126">Contenu de l’élément supplémentaire après les champs obligatoires, à moins que le **WS_STRUCT_IGNORE_TRAILING_ELEMENT_CONTENT**</span><span class="sxs-lookup"><span data-stu-id="61563-126">Extra element content after required fields, unless the **WS_STRUCT_IGNORE_TRAILING_ELEMENT_CONTENT**</span></span>
-   <span data-ttu-id="61563-127">Attributs inattendus, sauf si l’indicateur [**WS \_ struct \_ ignore les \_ \_ attributs non gérés**](https://msdn.microsoft.com/library/Dd323454(v=VS.85).aspx) est spécifié</span><span class="sxs-lookup"><span data-stu-id="61563-127">Unexpected attributes, unless [**WS\_STRUCT\_IGNORE\_UNHANDLED\_ATTRIBUTES**](https://msdn.microsoft.com/library/Dd323454(v=VS.85).aspx) flag is specified</span></span>
-   <span data-ttu-id="61563-128">Valeur de type de données inattendue en dehors de la plage spécifiée</span><span class="sxs-lookup"><span data-stu-id="61563-128">Unexpected data type value that is out of specified range</span></span>
-   <span data-ttu-id="61563-129">Le nombre d’éléments répétitifs est en dehors de la plage spécifiée</span><span class="sxs-lookup"><span data-stu-id="61563-129">Count of repeating element is out of the specified range</span></span>

<span data-ttu-id="61563-130">La sérialisation d’une grande quantité de données peut entraîner une allocation excessive de la mémoire et peut entraîner une attaque par déni de service.</span><span class="sxs-lookup"><span data-stu-id="61563-130">Serializing large amount of data might cause excessive memory allocation and can cause denial of service attack.</span></span> <span data-ttu-id="61563-131">L’utilisateur qui désérialise les données doit spécifier un objet segment de mémoire pour allouer les données, et l’utilisateur peut utiliser la limite d’allocation du tas pour empêcher une attaque d’allocation de mémoire.</span><span class="sxs-lookup"><span data-stu-id="61563-131">The user that is deserializing data must specify a Heap object to allocate the data, and the user can use the heap allocation limit to prevent memory allocation attack.</span></span>

<span data-ttu-id="61563-132">La prise en charge de plage pour les types de données, notamment la longueur maximale pour les chaînes, le nombre maximal d’éléments dans le tableau, etc. permet à l’utilisateur de contrôler la taille maximale des différents types de données.</span><span class="sxs-lookup"><span data-stu-id="61563-132">Range support for data types, including max length for string, max element count in array, etc. allows the user to control the maximum size for different data types.</span></span> <span data-ttu-id="61563-133">L’utilisateur peut spécifier une plage dans la description ou le schéma des données pour limiter la taille maximale des différentes données.</span><span class="sxs-lookup"><span data-stu-id="61563-133">User can specify range in data description or schema to limit the maximum size of different data.</span></span>

<span data-ttu-id="61563-134">Une valeur de chaîne contenant un zéro incorporé est prise en charge dans les formats de transmission (texte, binaire, MTOM).</span><span class="sxs-lookup"><span data-stu-id="61563-134">A string value containing an embedded zero is supported in the wire formats (text, binary, MTOM).</span></span> <span data-ttu-id="61563-135">Lors de la désérialisation d’une chaîne avec un zéro incorporé, l’utilisateur doit utiliser une chaîne comptée (WS \_ String) afin que le zéro ne confonde pas le calcul de la longueur de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="61563-135">When deserializing a string with an embedded zero, the user should use a counted string (WS\_STRING) so the zero will not confuse the calculation of the length of the string.</span></span> <span data-ttu-id="61563-136">Si une valeur de chaîne contenant un zéro incorporé est désérialisée dans un champ qui attend une chaîne se terminant par zéro, une erreur est retournée et la désérialisation échoue.</span><span class="sxs-lookup"><span data-stu-id="61563-136">If a string value containing an embedded zero is deserialized into a field that is expecting a zero-terminated string, an error is returned, and deserialization fails.</span></span> <span data-ttu-id="61563-137">Si Wsutil est utilisé pour générer des descriptions de données, l’option/String : WS \_ String doit être utilisée si la chaîne avec un zéro incorporé est attendue.</span><span class="sxs-lookup"><span data-stu-id="61563-137">If wsutil is used to generate data descriptions, /string:WS\_STRING option should be used if string with embedded zero is expected.</span></span>

<span data-ttu-id="61563-138">Les rappels suivants sont utilisés avec la sérialisation :</span><span class="sxs-lookup"><span data-stu-id="61563-138">The following callbacks are used with serialization:</span></span>

-   [<span data-ttu-id="61563-139">**rappel de comparaison de la \_ durée WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="61563-139">**WS\_DURATION\_COMPARISON\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_duration_comparison_callback)
-   [<span data-ttu-id="61563-140">**\_rappel de \_ type WS Read \_**</span><span class="sxs-lookup"><span data-stu-id="61563-140">**WS\_READ\_TYPE\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_read_type_callback)
-   [<span data-ttu-id="61563-141">**\_rappel de \_ type WS Write \_**</span><span class="sxs-lookup"><span data-stu-id="61563-141">**WS\_WRITE\_TYPE\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_write_type_callback)

<span data-ttu-id="61563-142">Les énumérations suivantes sont utilisées avec la sérialisation :</span><span class="sxs-lookup"><span data-stu-id="61563-142">The following enumerations are used with serialization:</span></span>

-   [<span data-ttu-id="61563-143">**\_mappage de champs WS \_**</span><span class="sxs-lookup"><span data-stu-id="61563-143">**WS\_FIELD\_MAPPING**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_field_mapping)
-   [<span data-ttu-id="61563-144">**\_options de champ WS \_**</span><span class="sxs-lookup"><span data-stu-id="61563-144">**WS\_FIELD\_OPTIONS**</span></span>](/windows/win32/api/webservices/ne-webservices-ws_xml_reader_encoding_type)
-   [<span data-ttu-id="61563-145">**\_option WS Read \_**</span><span class="sxs-lookup"><span data-stu-id="61563-145">**WS\_READ\_OPTION**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_read_option)
-   [<span data-ttu-id="61563-146">**\_type WS**</span><span class="sxs-lookup"><span data-stu-id="61563-146">**WS\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_type)
-   [<span data-ttu-id="61563-147">**\_mappage de type WS \_**</span><span class="sxs-lookup"><span data-stu-id="61563-147">**WS\_TYPE\_MAPPING**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_type_mapping)
-   [<span data-ttu-id="61563-148">**\_option d’écriture WS \_**</span><span class="sxs-lookup"><span data-stu-id="61563-148">**WS\_WRITE\_OPTION**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_write_option)

<span data-ttu-id="61563-149">Les fonctions suivantes sont utilisées avec la sérialisation :</span><span class="sxs-lookup"><span data-stu-id="61563-149">The following functions are used with serialization:</span></span>

-   [<span data-ttu-id="61563-150">**WsReadAttribute**</span><span class="sxs-lookup"><span data-stu-id="61563-150">**WsReadAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadattribute)
-   [<span data-ttu-id="61563-151">**WsReadElement**</span><span class="sxs-lookup"><span data-stu-id="61563-151">**WsReadElement**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadelement)
-   [<span data-ttu-id="61563-152">**WsReadType**</span><span class="sxs-lookup"><span data-stu-id="61563-152">**WsReadType**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadtype)
-   [<span data-ttu-id="61563-153">**WsWriteAttribute**</span><span class="sxs-lookup"><span data-stu-id="61563-153">**WsWriteAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswriteattribute)
-   [<span data-ttu-id="61563-154">**WsWriteElement**</span><span class="sxs-lookup"><span data-stu-id="61563-154">**WsWriteElement**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswriteelement)
-   [<span data-ttu-id="61563-155">**WsWriteType**</span><span class="sxs-lookup"><span data-stu-id="61563-155">**WsWriteType**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritetype)

<span data-ttu-id="61563-156">Les structures suivantes sont utilisées avec la sérialisation :</span><span class="sxs-lookup"><span data-stu-id="61563-156">The following structures are used with serialization:</span></span>

-   [<span data-ttu-id="61563-157">**Description de l' \_ attribut WS \_**</span><span class="sxs-lookup"><span data-stu-id="61563-157">**WS\_ATTRIBUTE\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_attribute_description)
-   [<span data-ttu-id="61563-158">**\_Description WS bool \_**</span><span class="sxs-lookup"><span data-stu-id="61563-158">**WS\_BOOL\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_bool_description)
-   [<span data-ttu-id="61563-159">**Description de WS \_ octets \_**</span><span class="sxs-lookup"><span data-stu-id="61563-159">**WS\_BYTES\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_bytes_description)
-   [<span data-ttu-id="61563-160">**\_Description du \_ tableau WS Byte \_**</span><span class="sxs-lookup"><span data-stu-id="61563-160">**WS\_BYTE\_ARRAY\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_byte_array_description)
-   [<span data-ttu-id="61563-161">**\_Description du \_ tableau de caractères WS \_**</span><span class="sxs-lookup"><span data-stu-id="61563-161">**WS\_CHAR\_ARRAY\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_char_array_description)
-   [<span data-ttu-id="61563-162">**\_Description du \_ type \_ personnalisé WS**</span><span class="sxs-lookup"><span data-stu-id="61563-162">**WS\_CUSTOM\_TYPE\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_custom_type_description)
-   [<span data-ttu-id="61563-163">**Description de WS \_ DateTime \_**</span><span class="sxs-lookup"><span data-stu-id="61563-163">**WS\_DATETIME\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_datetime_description)
-   [<span data-ttu-id="61563-164">**Description de WS \_ Decimal \_**</span><span class="sxs-lookup"><span data-stu-id="61563-164">**WS\_DECIMAL\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_decimal_description)
-   [<span data-ttu-id="61563-165">**\_valeur par défaut de WS \_**</span><span class="sxs-lookup"><span data-stu-id="61563-165">**WS\_DEFAULT\_VALUE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_default_value)
-   [<span data-ttu-id="61563-166">**Description de WS \_ double \_**</span><span class="sxs-lookup"><span data-stu-id="61563-166">**WS\_DOUBLE\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_double_description)
-   [<span data-ttu-id="61563-167">**Description de la \_ durée WS \_**</span><span class="sxs-lookup"><span data-stu-id="61563-167">**WS\_DURATION\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_duration_description)
-   [<span data-ttu-id="61563-168">**Description de l' \_ élément WS \_**</span><span class="sxs-lookup"><span data-stu-id="61563-168">**WS\_ELEMENT\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_element_description)
-   [<span data-ttu-id="61563-169">**Description de l' \_ adresse du point de terminaison WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="61563-169">**WS\_ENDPOINT\_ADDRESS\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address_description)
-   [<span data-ttu-id="61563-170">**Description de WS \_ enum \_**</span><span class="sxs-lookup"><span data-stu-id="61563-170">**WS\_ENUM\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_enum_description)
-   [<span data-ttu-id="61563-171">**\_valeur d’énumération WS \_**</span><span class="sxs-lookup"><span data-stu-id="61563-171">**WS\_ENUM\_VALUE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_enum_value)
-   [<span data-ttu-id="61563-172">**Description de l' \_ erreur WS \_**</span><span class="sxs-lookup"><span data-stu-id="61563-172">**WS\_FAULT\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_fault_description)
-   [<span data-ttu-id="61563-173">**\_Description du champ WS \_**</span><span class="sxs-lookup"><span data-stu-id="61563-173">**WS\_FIELD\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_field_description)
-   [<span data-ttu-id="61563-174">**\_Description WS float \_**</span><span class="sxs-lookup"><span data-stu-id="61563-174">**WS\_FLOAT\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_float_description)
-   [<span data-ttu-id="61563-175">**\_Description du GUID WS \_**</span><span class="sxs-lookup"><span data-stu-id="61563-175">**WS\_GUID\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_guid_description)
-   [<span data-ttu-id="61563-176">**\_Description WS Int16 \_**</span><span class="sxs-lookup"><span data-stu-id="61563-176">**WS\_INT16\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_int16_description)
-   [<span data-ttu-id="61563-177">**\_Description WS Int32 \_**</span><span class="sxs-lookup"><span data-stu-id="61563-177">**WS\_INT32\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_int32_description)
-   [<span data-ttu-id="61563-178">**\_Description WS Int64 \_**</span><span class="sxs-lookup"><span data-stu-id="61563-178">**WS\_INT64\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_int64_description)
-   [<span data-ttu-id="61563-179">**Description de WS \_ INT8 \_**</span><span class="sxs-lookup"><span data-stu-id="61563-179">**WS\_INT8\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_int8_description)
-   [<span data-ttu-id="61563-180">**\_plage d’éléments WS \_**</span><span class="sxs-lookup"><span data-stu-id="61563-180">**WS\_ITEM\_RANGE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_item_range)
-   [<span data-ttu-id="61563-181">**Description de la \_ chaîne WS \_**</span><span class="sxs-lookup"><span data-stu-id="61563-181">**WS\_STRING\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_string_description)
-   [<span data-ttu-id="61563-182">**Description de WS \_ struct \_**</span><span class="sxs-lookup"><span data-stu-id="61563-182">**WS\_STRUCT\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_struct_description)
-   [<span data-ttu-id="61563-183">**\_Description WS TIMESPAN \_**</span><span class="sxs-lookup"><span data-stu-id="61563-183">**WS\_TIMESPAN\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_timespan_description)
-   [<span data-ttu-id="61563-184">**Description de WS \_ UINT16 \_**</span><span class="sxs-lookup"><span data-stu-id="61563-184">**WS\_UINT16\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_uint16_description)
-   [<span data-ttu-id="61563-185">**Description de WS \_ UInt32 \_**</span><span class="sxs-lookup"><span data-stu-id="61563-185">**WS\_UINT32\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_uint32_description)
-   [<span data-ttu-id="61563-186">**\_Description WS UINT64 \_**</span><span class="sxs-lookup"><span data-stu-id="61563-186">**WS\_UINT64\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_uint64_description)
-   [<span data-ttu-id="61563-187">**Description de WS \_ UINT8 \_**</span><span class="sxs-lookup"><span data-stu-id="61563-187">**WS\_UINT8\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_uint8_description)
-   [<span data-ttu-id="61563-188">**Description de WS \_ Union \_**</span><span class="sxs-lookup"><span data-stu-id="61563-188">**WS\_UNION\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_union_description)
-   [<span data-ttu-id="61563-189">**\_Description du \_ champ WS Union \_**</span><span class="sxs-lookup"><span data-stu-id="61563-189">**WS\_UNION\_FIELD\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_union_field_description)
-   [<span data-ttu-id="61563-190">**Description de l' \_ ID unique de WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="61563-190">**WS\_UNIQUE\_ID\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_unique_id_description)
-   [<span data-ttu-id="61563-191">**\_Description du \_ tableau WS UTF8 \_**</span><span class="sxs-lookup"><span data-stu-id="61563-191">**WS\_UTF8\_ARRAY\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_utf8_array_description)
-   [<span data-ttu-id="61563-192">**Description de WS \_ void \_**</span><span class="sxs-lookup"><span data-stu-id="61563-192">**WS\_VOID\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_void_description)
-   [<span data-ttu-id="61563-193">**Description de WS \_ WSZ \_**</span><span class="sxs-lookup"><span data-stu-id="61563-193">**WS\_WSZ\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_wsz_description)
-   [<span data-ttu-id="61563-194">**\_Description du \_ QName \_ XML WS**</span><span class="sxs-lookup"><span data-stu-id="61563-194">**WS\_XML\_QNAME\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_qname_description)
-   [<span data-ttu-id="61563-195">**Description de la \_ chaîne XML WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="61563-195">**WS\_XML\_STRING\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string_description)

 

 




