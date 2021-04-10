---
description: La structure de données PROPERTYINFO définit une propriété du protocole.
ms.assetid: 878777ab-141d-4cc5-b0c1-f2ac8f770bf0
title: PROPERTYINFO, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROPERTYINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 435b08c5dd5e020dce2bde9be03a0d41299836c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951736"
---
# <a name="propertyinfo-structure"></a><span data-ttu-id="05903-103">PROPERTYINFO, structure</span><span class="sxs-lookup"><span data-stu-id="05903-103">PROPERTYINFO structure</span></span>

<span data-ttu-id="05903-104">La structure de données **PROPERTYINFO** définit une propriété du protocole.</span><span class="sxs-lookup"><span data-stu-id="05903-104">The **PROPERTYINFO** data structure defines one property of the protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="05903-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="05903-105">Syntax</span></span>


```C++
typedef struct _PROPERTYINFO {
  HPROPERTY hProperty;
  DWORD     Version;
  LPSTR     Label;
  LPSTR     Comment;
  BYTE      DataType;
  BYTE      DataQualifier;
  union {
    LPVOID  lpExtendedInfo;
    LPRANGE lpRange;
    LPSET   lpSet;
    DWORD   Bitmask;
    DWORD   Value;
  };
  WORD      FormatStringSize;
  LPVOID    InstanceData;
} PROPERTYINFO, *LPPROPERTYINFO;
```



## <a name="members"></a><span data-ttu-id="05903-106">Membres</span><span class="sxs-lookup"><span data-stu-id="05903-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="05903-107">**hProperty**</span><span class="sxs-lookup"><span data-stu-id="05903-107">**hProperty**</span></span>
</dt> <dd>

<span data-ttu-id="05903-108">Définissez ce champ sur zéro.</span><span class="sxs-lookup"><span data-stu-id="05903-108">Set this field to zero.</span></span> <span data-ttu-id="05903-109">Lors de la sortie, Moniteur réseau retourne un handle vers la propriété après que la propriété a été ajoutée à la base de données de propriétés.</span><span class="sxs-lookup"><span data-stu-id="05903-109">On output, Network Monitor returns a handle to the property after the property is added to the property database.</span></span>

</dd> <dt>

<span data-ttu-id="05903-110">**Version**</span><span class="sxs-lookup"><span data-stu-id="05903-110">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="05903-111">Réservé.</span><span class="sxs-lookup"><span data-stu-id="05903-111">Reserved.</span></span> <span data-ttu-id="05903-112">Doit être défini à zéro.</span><span class="sxs-lookup"><span data-stu-id="05903-112">Must be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="05903-113">**Étiquette**</span><span class="sxs-lookup"><span data-stu-id="05903-113">**Label**</span></span>
</dt> <dd>

<span data-ttu-id="05903-114">Nom de la propriété.</span><span class="sxs-lookup"><span data-stu-id="05903-114">Name of the property.</span></span>

</dd> <dt>

<span data-ttu-id="05903-115">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="05903-115">**Comment**</span></span>
</dt> <dd>

<span data-ttu-id="05903-116">Description de la propriété.</span><span class="sxs-lookup"><span data-stu-id="05903-116">Description of the property.</span></span> <span data-ttu-id="05903-117">La description s’affiche dans la barre d’État Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="05903-117">The description appears on the Network Monitor status bar.</span></span>

</dd> <dt>

<span data-ttu-id="05903-118">**DataType**</span><span class="sxs-lookup"><span data-stu-id="05903-118">**DataType**</span></span>
</dt> <dd>

<span data-ttu-id="05903-119">Type de données de la propriété.</span><span class="sxs-lookup"><span data-stu-id="05903-119">Data type of the property.</span></span> <span data-ttu-id="05903-120">Ce membre peut avoir l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="05903-120">This member can have one of the following values.</span></span>



| <span data-ttu-id="05903-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="05903-121">Value</span></span>                                                                                                                                                                                                       | <span data-ttu-id="05903-122">Signification</span><span class="sxs-lookup"><span data-stu-id="05903-122">Meaning</span></span>                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROP_TYPE_VOID"></span><span id="prop_type_void"></span><dl> <span data-ttu-id="05903-123"><dt>**PROP, \_ type \_ void**</dt></span><span class="sxs-lookup"><span data-stu-id="05903-123"><dt>**PROP\_TYPE\_VOID**</dt></span></span> </dl>                                           | <span data-ttu-id="05903-124">Le type de propriété est inconnu.</span><span class="sxs-lookup"><span data-stu-id="05903-124">Property type is unknown.</span></span> <span data-ttu-id="05903-125">Il n’existe pas de longueur ou de format implicite.</span><span class="sxs-lookup"><span data-stu-id="05903-125">There is no implied length or format.</span></span><br/>                                                                                                                                                                                                                                  |
| <span id="PROP_TYPE_SUMMARY"></span><span id="prop_type_summary"></span><dl> <span data-ttu-id="05903-126"><dt>**\_Résumé du type de prop \_**</dt></span><span class="sxs-lookup"><span data-stu-id="05903-126"><dt>**PROP\_TYPE\_SUMMARY**</dt></span></span> </dl>                                  | <span data-ttu-id="05903-127">Résumé du type de propriété.</span><span class="sxs-lookup"><span data-stu-id="05903-127">Summarizing property type.</span></span> <span data-ttu-id="05903-128">Indique la première instance de propriété que l’analyseur attache à un frame.</span><span class="sxs-lookup"><span data-stu-id="05903-128">Indicates the first property instance that the parser attaches to a frame.</span></span> <span data-ttu-id="05903-129">\_ \_ Le résumé du type prop peut servir d’espace réservé pour les groupes de propriétés.</span><span class="sxs-lookup"><span data-stu-id="05903-129">PROP\_TYPE\_SUMMARY can serve as a placeholder for groups of properties.</span></span> <span data-ttu-id="05903-130">Cette valeur indique que la propriété n’est pas définie dans le protocole *RFC*.</span><span class="sxs-lookup"><span data-stu-id="05903-130">This value indicates that the property is not defined in the protocol *RFC*.</span></span><br/> |
| <span id="PROP_TYPE_BYTE"></span><span id="prop_type_byte"></span><dl> <span data-ttu-id="05903-131"><dt>**\_octet de type prop \_**</dt></span><span class="sxs-lookup"><span data-stu-id="05903-131"><dt>**PROP\_TYPE\_BYTE**</dt></span></span> </dl>                                           | <span data-ttu-id="05903-132">Données numériques d’une taille d’un octet (entité 8 bits).</span><span class="sxs-lookup"><span data-stu-id="05903-132">Numeric data with a size of one byte (8-bit entity).</span></span><br/>                                                                                                                                                                                                                                             |
| <span id="PROP_TYPE_WORD"></span><span id="prop_type_word"></span><dl> <span data-ttu-id="05903-133"><dt>**PROP, \_ type \_ Word**</dt></span><span class="sxs-lookup"><span data-stu-id="05903-133"><dt>**PROP\_TYPE\_WORD**</dt></span></span> </dl>                                           | <span data-ttu-id="05903-134">Données numériques d’une taille de deux octets (entité 16 bits).</span><span class="sxs-lookup"><span data-stu-id="05903-134">Numeric data with a size of two bytes (16-bit entity).</span></span><br/>                                                                                                                                                                                                                                           |
| <span id="PROP_TYPE_DWORD"></span><span id="prop_type_dword"></span><dl> <span data-ttu-id="05903-135"><dt>**TYPE de PROP \_ \_ DWORD**</dt></span><span class="sxs-lookup"><span data-stu-id="05903-135"><dt>**PROP\_TYPE\_DWORD**</dt></span></span> </dl>                                        | <span data-ttu-id="05903-136">Données numériques d’une taille de 4 octets (entité 32 bits).</span><span class="sxs-lookup"><span data-stu-id="05903-136">Numeric data with a size of four bytes (32-bit entity).</span></span><br/>                                                                                                                                                                                                                                          |
| <span id="PROP_TYPE_LARGEINT"></span><span id="prop_type_largeint"></span><dl> <span data-ttu-id="05903-137"><dt>**PROP, \_ type \_ LARGEINT**</dt></span><span class="sxs-lookup"><span data-stu-id="05903-137"><dt>**PROP\_TYPE\_LARGEINT**</dt></span></span> </dl>                               | <span data-ttu-id="05903-138">Données numériques d’une taille de huit octets (entité 64 bits).</span><span class="sxs-lookup"><span data-stu-id="05903-138">Numeric data with a size of eight bytes (64-bit entity).</span></span><br/>                                                                                                                                                                                                                                         |
| <span id="PROP_TYPE_ADDR"></span><span id="prop_type_addr"></span><dl> <span data-ttu-id="05903-139"><dt>**\_ADR type \_ addr**</dt></span><span class="sxs-lookup"><span data-stu-id="05903-139"><dt>**PROP\_TYPE\_ADDR**</dt></span></span> </dl>                                           | <span data-ttu-id="05903-140">Adresse MAC (entité de 6 octets).</span><span class="sxs-lookup"><span data-stu-id="05903-140">MAC address (6-byte entity).</span></span><br/>                                                                                                                                                                                                                                                                     |
| <span id="PROP_TYPE_TIME"></span><span id="prop_type_time"></span><dl> <span data-ttu-id="05903-141"><dt>**\_heure du type de prop \_**</dt></span><span class="sxs-lookup"><span data-stu-id="05903-141"><dt>**PROP\_TYPE\_TIME**</dt></span></span> </dl>                                           | <span data-ttu-id="05903-142">Structure **SystemTime** .</span><span class="sxs-lookup"><span data-stu-id="05903-142">**SYSTEMTIME** structure.</span></span><br/>                                                                                                                                                                                                                                                                        |
| <span id="PROP_TYPE_STRING"></span><span id="prop_type_string"></span><dl> <span data-ttu-id="05903-143"><dt>**\_chaîne de type prop \_**</dt></span><span class="sxs-lookup"><span data-stu-id="05903-143"><dt>**PROP\_TYPE\_STRING**</dt></span></span> </dl>                                     | <span data-ttu-id="05903-144">Données texte ASCII.</span><span class="sxs-lookup"><span data-stu-id="05903-144">ASCII text data.</span></span> <span data-ttu-id="05903-145">Ce type de données ne se termine pas par un caractère NULL.</span><span class="sxs-lookup"><span data-stu-id="05903-145">This data type is not NULL-terminated.</span></span> <br/> <span data-ttu-id="05903-146">Pour les données Unicode, lorsque les données de texte ASCII sont spécifiées, l' \_ Indicateur Unicode IFLAG doit également être défini lorsque la fonction d’instance de propriété Attach est appelée.</span><span class="sxs-lookup"><span data-stu-id="05903-146">For Unicode data, when ASCII text data is specified, the IFLAG\_UNICODE flag must also be set when the attach property instance function is called.</span></span><br/>                                                                          |
| <span id="PROP_TYPE_IP_ADDRESS"></span><span id="prop_type_ip_address"></span><dl> <span data-ttu-id="05903-147"><dt>**\_ \_ adresse IP du type de prop \_**</dt></span><span class="sxs-lookup"><span data-stu-id="05903-147"><dt>**PROP\_TYPE\_IP\_ADDRESS**</dt></span></span> </dl>                        | <span data-ttu-id="05903-148">Adresse IP.</span><span class="sxs-lookup"><span data-stu-id="05903-148">IP Address.</span></span> <span data-ttu-id="05903-149">(entité de 4 octets).</span><span class="sxs-lookup"><span data-stu-id="05903-149">(4-byte entity).</span></span><br/>                                                                                                                                                                                                                                                                     |
| <span id="PROP_TYPE_IPX_ADDRESS"></span><span id="prop_type_ipx_address"></span><dl> <span data-ttu-id="05903-150"><dt>**\_ \_ adresse IPX du type prop \_**</dt></span><span class="sxs-lookup"><span data-stu-id="05903-150"><dt>**PROP\_TYPE\_IPX\_ADDRESS**</dt></span></span> </dl>                     | <span data-ttu-id="05903-151">Adresse IPX.</span><span class="sxs-lookup"><span data-stu-id="05903-151">IPX Address.</span></span> <span data-ttu-id="05903-152">(entité de 10 octets).</span><span class="sxs-lookup"><span data-stu-id="05903-152">(10-byte entity).</span></span><br/>                                                                                                                                                                                                                                                                   |
| <span id="PROP_TYPE_BYTESWAPPED_WORD"></span><span id="prop_type_byteswapped_word"></span><dl> <span data-ttu-id="05903-153"><dt>**PROP, \_ type \_ BYTESWAPPED \_ mot**</dt></span><span class="sxs-lookup"><span data-stu-id="05903-153"><dt>**PROP\_TYPE\_BYTESWAPPED\_WORD**</dt></span></span> </dl>      | <span data-ttu-id="05903-154">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="05903-154">Obsolete.</span></span> <span data-ttu-id="05903-155">Pour les données de mot avec échange d’octets, définissez **DataType** sur Prop \_ type \_ Word et définissez l' \_ indicateur permuté IFLAG lors de l’appel d’une fonction d’instance de propriété **Attach** .</span><span class="sxs-lookup"><span data-stu-id="05903-155">For byte-swapped WORD data, set **DataType** to PROP\_TYPE\_WORD and set the IFLAG\_SWAPPED flag when calling an **Attach** property instance function.</span></span><br/>                                                                                                                                |
| <span id="PROP_TYPE_BYTESWAPPED_DWORD"></span><span id="prop_type_byteswapped_dword"></span><dl> <span data-ttu-id="05903-156"><dt>**PROP \_ type \_ BYTESWAPPED \_ DWORD**</dt></span><span class="sxs-lookup"><span data-stu-id="05903-156"><dt>**PROP\_TYPE\_BYTESWAPPED\_DWORD**</dt></span></span> </dl>   | <span data-ttu-id="05903-157">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="05903-157">Obsolete.</span></span> <span data-ttu-id="05903-158">Pour les données DWORD échangées en octets, définissez **DataType** sur Prop \_ type \_ DWORD et définissez l' \_ indicateur permuté IFLAG lors de l’appel d’une fonction d’instance de propriété **Attach** .</span><span class="sxs-lookup"><span data-stu-id="05903-158">For byte-swapped DWORD data, set **DataType** to PROP\_TYPE\_DWORD and set the IFLAG\_SWAPPED flag when calling an **Attach** property instance function.</span></span><br/>                                                                                                                              |
| <span id="PROP_TYPE_TYPED_STRING"></span><span id="prop_type_typed_string"></span><dl> <span data-ttu-id="05903-159"><dt>**\_ \_ chaîne typée de type prop \_**</dt></span><span class="sxs-lookup"><span data-stu-id="05903-159"><dt>**PROP\_TYPE\_TYPED\_STRING**</dt></span></span> </dl>                  | <span data-ttu-id="05903-160">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="05903-160">Obsolete.</span></span> <span data-ttu-id="05903-161">Pour les données de type chaîne de type variable, définissez **DataType** sur \_ type de \_ chaîne et définissez l' \_ Indicateur Unicode IFLAG lors de l’appel d’une fonction d’instance de propriété **Attach** .</span><span class="sxs-lookup"><span data-stu-id="05903-161">For variable-type string data, set **DataType** to PROP\_TYPE\_STRING and set the IFLAG\_UNICODE flag when calling an **Attach** property instance function.</span></span><br/>                                                                                                                           |
| <span id="PROP_TYPE_RAW_DATA"></span><span id="prop_type_raw_data"></span><dl> <span data-ttu-id="05903-162"><dt>**\_ \_ données brutes de type prop \_**</dt></span><span class="sxs-lookup"><span data-stu-id="05903-162"><dt>**PROP\_TYPE\_RAW\_DATA**</dt></span></span> </dl>                              | <span data-ttu-id="05903-163">Données brutes de longueur et de format inconnues.</span><span class="sxs-lookup"><span data-stu-id="05903-163">Raw data of unknown length and format.</span></span><br/>                                                                                                                                                                                                                                                           |
| <span id="PROP_TYPE_COMMENT"></span><span id="prop_type_comment"></span><dl> <span data-ttu-id="05903-164"><dt>**Commentaire sur le \_ type prop \_**</dt></span><span class="sxs-lookup"><span data-stu-id="05903-164"><dt>**PROP\_TYPE\_COMMENT**</dt></span></span> </dl>                                  | <span data-ttu-id="05903-165">Identique au type PROP, \_ \_ void.</span><span class="sxs-lookup"><span data-stu-id="05903-165">Same as PROP\_TYPE\_VOID.</span></span><br/>                                                                                                                                                                                                                                                                        |
| <span id="PROP_TYPE_SRCFRIENDLYNAME"></span><span id="prop_type_srcfriendlyname"></span><dl> <span data-ttu-id="05903-166"><dt>**PROP, \_ type \_ SRCFRIENDLYNAME**</dt></span><span class="sxs-lookup"><span data-stu-id="05903-166"><dt>**PROP\_TYPE\_SRCFRIENDLYNAME**</dt></span></span> </dl>          | <span data-ttu-id="05903-167">Adresse du nom convivial de la source.</span><span class="sxs-lookup"><span data-stu-id="05903-167">Address of source-friendly name.</span></span> <span data-ttu-id="05903-168">Moniteur réseau ne fournit pas de prise en charge intégrée de la mise en forme pour ce type de données.</span><span class="sxs-lookup"><span data-stu-id="05903-168">Network Monitor does not provide built-in formatting support for this data type.</span></span><br/>                                                                                                                                                                                |
| <span id="PROP_TYPE_DSTFRIENDLYNAME"></span><span id="prop_type_dstfriendlyname"></span><dl> <span data-ttu-id="05903-169"><dt>**PROP, \_ type \_ DSTFRIENDLYNAME**</dt></span><span class="sxs-lookup"><span data-stu-id="05903-169"><dt>**PROP\_TYPE\_DSTFRIENDLYNAME**</dt></span></span> </dl>          | <span data-ttu-id="05903-170">Adresse du nom convivial de destination.</span><span class="sxs-lookup"><span data-stu-id="05903-170">Address of destination friendly name.</span></span> <span data-ttu-id="05903-171">Moniteur réseau ne fournit pas de prise en charge intégrée de la mise en forme pour ce type de données.</span><span class="sxs-lookup"><span data-stu-id="05903-171">Network Monitor does not provide built-in formatting support for this data type.</span></span><br/>                                                                                                                                                                           |
| <span id="PROP_TYPE_TOKENRING_ADDRESS"></span><span id="prop_type_tokenring_address"></span><dl> <span data-ttu-id="05903-172"><dt>**\_ \_ adresse TOKENRING de type prop \_**</dt></span><span class="sxs-lookup"><span data-stu-id="05903-172"><dt>**PROP\_TYPE\_TOKENRING\_ADDRESS**</dt></span></span> </dl>   | <span data-ttu-id="05903-173">Adresse Token Ring.</span><span class="sxs-lookup"><span data-stu-id="05903-173">Token-ring address.</span></span> <span data-ttu-id="05903-174">Moniteur réseau ne fournit pas de prise en charge intégrée de la mise en forme pour ce type de données.</span><span class="sxs-lookup"><span data-stu-id="05903-174">Network Monitor does not provide built-in formatting support for this data type.</span></span><br/>                                                                                                                                                                                             |
| <span id="PROP_TYPE_FDDI_ADDRESS"></span><span id="prop_type_fddi_address"></span><dl> <span data-ttu-id="05903-175"><dt>**\_ \_ adresse FDDI du type de prop \_**</dt></span><span class="sxs-lookup"><span data-stu-id="05903-175"><dt>**PROP\_TYPE\_FDDI\_ADDRESS**</dt></span></span> </dl>                  | <span data-ttu-id="05903-176">Adresse FDDI.</span><span class="sxs-lookup"><span data-stu-id="05903-176">FDDI address.</span></span> <span data-ttu-id="05903-177">Moniteur réseau ne fournit pas de prise en charge intégrée de la mise en forme pour ce type de données.</span><span class="sxs-lookup"><span data-stu-id="05903-177">Network Monitor does not provide built-in formatting support for this data type.</span></span><br/>                                                                                                                                                                                                   |
| <span id="PROP_TYPE_ETHERNET_ADDRESS"></span><span id="prop_type_ethernet_address"></span><dl> <span data-ttu-id="05903-178"><dt>**\_ \_ adresse Ethernet du type prop \_**</dt></span><span class="sxs-lookup"><span data-stu-id="05903-178"><dt>**PROP\_TYPE\_ETHERNET\_ADDRESS**</dt></span></span> </dl>      | <span data-ttu-id="05903-179">Adresse Ethernet.</span><span class="sxs-lookup"><span data-stu-id="05903-179">Ethernet address.</span></span> <span data-ttu-id="05903-180">Moniteur réseau ne fournit pas de prise en charge intégrée de la mise en forme pour ce type de données.</span><span class="sxs-lookup"><span data-stu-id="05903-180">Network Monitor does not provide built-in formatting support for this data type.</span></span><br/>                                                                                                                                                                                               |
| <span id="PROP_TYPE_OBJECT_IDENTIFIER"></span><span id="prop_type_object_identifier"></span><dl> <span data-ttu-id="05903-181"><dt>**\_identificateur d' \_ objet du type prop \_**</dt></span><span class="sxs-lookup"><span data-stu-id="05903-181"><dt>**PROP\_TYPE\_OBJECT\_IDENTIFIER**</dt></span></span> </dl>   | <span data-ttu-id="05903-182">Identificateur d’objet SNMP encodé BER.</span><span class="sxs-lookup"><span data-stu-id="05903-182">BER-encoded SNMP object identifier.</span></span><br/>                                                                                                                                                                                                                                                              |
| <span id="PROP_TYPE_VINES_IP_ADDRESS"></span><span id="prop_type_vines_ip_address"></span><dl> <span data-ttu-id="05903-183"><dt>**\_ \_ \_ adresse IP du type de props \_**</dt></span><span class="sxs-lookup"><span data-stu-id="05903-183"><dt>**PROP\_TYPE\_VINES\_IP\_ADDRESS**</dt></span></span> </dl>     | <span data-ttu-id="05903-184">Adresse IP Vines (entité de 6 octets).</span><span class="sxs-lookup"><span data-stu-id="05903-184">Vines IP address (6-byte entity).</span></span><br/>                                                                                                                                                                                                                                                                |
| <span id="PROP_TYPE_VAR_LEN_SMALL_INT"></span><span id="prop_type_var_len_small_int"></span><dl> <span data-ttu-id="05903-185"><dt>**PROP \_ type \_ var \_ Len \_ petit \_ int**</dt></span><span class="sxs-lookup"><span data-stu-id="05903-185"><dt>**PROP\_TYPE\_VAR\_LEN\_SMALL\_INT**</dt></span></span> </dl> | <span data-ttu-id="05903-186">Valeur numérique sans longueur prédéfinie, mais inférieure à 8 octets.</span><span class="sxs-lookup"><span data-stu-id="05903-186">Numeric value without a pre-determined length, but no more than 8 bytes long.</span></span> <span data-ttu-id="05903-187">La longueur des données attachées détermine la longueur de la valeur.</span><span class="sxs-lookup"><span data-stu-id="05903-187">The length of the attached data determines the length of the value.</span></span><br/>                                                                                                                                                |



 

</dd> <dt>

<span data-ttu-id="05903-188">**DataQualifier**</span><span class="sxs-lookup"><span data-stu-id="05903-188">**DataQualifier**</span></span>
</dt> <dd>

<span data-ttu-id="05903-189">Qualificateur de données d’une propriété.</span><span class="sxs-lookup"><span data-stu-id="05903-189">The data qualifier of a property.</span></span> <span data-ttu-id="05903-190">Ce membre fournit des informations précises sur le type de données.</span><span class="sxs-lookup"><span data-stu-id="05903-190">This member provides precise information about the data type.</span></span>

<span data-ttu-id="05903-191">**DataQualifier** peut avoir l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="05903-191">**DataQualifier** can have one of the following values.</span></span>



| <span data-ttu-id="05903-192">Valeur</span><span class="sxs-lookup"><span data-stu-id="05903-192">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="05903-193">Signification</span><span class="sxs-lookup"><span data-stu-id="05903-193">Meaning</span></span>                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROP_QUAL_NONE"></span><span id="prop_qual_none"></span><dl> <span data-ttu-id="05903-194"><dt>**PROP \_ Qualys \_ None**</dt></span><span class="sxs-lookup"><span data-stu-id="05903-194"><dt>**PROP\_QUAL\_NONE**</dt></span></span> </dl>                                      | <span data-ttu-id="05903-195">Le type de données de la propriété est la seule spécification de la propriété.</span><span class="sxs-lookup"><span data-stu-id="05903-195">The property data type is the only specification of the property.</span></span> <br/> <span data-ttu-id="05903-196">Lorsque cette valeur est définie, le membre Union de la structure a la valeur **null**, puis est ignoré.</span><span class="sxs-lookup"><span data-stu-id="05903-196">When this value is set, the union member of the structure is set to **NULL**, and then ignored.</span></span><br/>                                                                                                                                        |
| <span id="PROP_QUAL_RANGE"></span><span id="prop_qual_range"></span><dl> <span data-ttu-id="05903-197"><dt>**plage de compétences PROP \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="05903-197"><dt>**PROP\_QUAL\_RANGE**</dt></span></span> </dl>                                   | <span data-ttu-id="05903-198">La valeur numérique doit être comprise dans une plage donnée.</span><span class="sxs-lookup"><span data-stu-id="05903-198">The numeric value is expected to be within a given range.</span></span> <span data-ttu-id="05903-199">Définissez la plage dans le membre **lpRange** .</span><span class="sxs-lookup"><span data-stu-id="05903-199">Define the range in the **lpRange** member.</span></span><br/>                                                                                                                                                                                                                |
| <span id="PROP_QUAL_SET"></span><span id="prop_qual_set"></span><dl> <span data-ttu-id="05903-200"><dt>**ensemble de compétences PROP \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="05903-200"><dt>**PROP\_QUAL\_SET**</dt></span></span> </dl>                                         | <span data-ttu-id="05903-201">La valeur d’une propriété est comparée à un ensemble de valeurs spécifiées dans le membre **lpSet** de l’Union de la structure.</span><span class="sxs-lookup"><span data-stu-id="05903-201">The value of a property is compared to a set of values that are specified in the **lpSet** member of the structure's union.</span></span> <span data-ttu-id="05903-202">La valeur d’une propriété peut être un **octet**, un **mot**, un **DWORD**, un **LARGEINT** ou une **heure**.</span><span class="sxs-lookup"><span data-stu-id="05903-202">The value of a property can be a **BYTE**, **WORD**, **DWORD**, **LARGEINT** or **TIME**.</span></span><br/>                                                                                                |
| <span id="PROP_QUAL_BITFIELD"></span><span id="prop_qual_bitfield"></span><dl> <span data-ttu-id="05903-203"><dt>**\_champ de \_ binaire prop Qualys**</dt></span><span class="sxs-lookup"><span data-stu-id="05903-203"><dt>**PROP\_QUAL\_BITFIELD**</dt></span></span> </dl>                          | <span data-ttu-id="05903-204">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="05903-204">Obsolete.</span></span><br/>                                                                                                                                                                                                                                                                                                            |
| <span id="PROP_QUAL_LABELED_SET"></span><span id="prop_qual_labeled_set"></span><dl> <span data-ttu-id="05903-205"><dt>**PROP \_ prop \_ étiquetée \_ Set**</dt></span><span class="sxs-lookup"><span data-stu-id="05903-205"><dt>**PROP\_QUAL\_LABELED\_SET**</dt></span></span> </dl>                | <span data-ttu-id="05903-206">La valeur d’une propriété est comparée à une valeur d’un ensemble de paires d’étiquettes de valeur.</span><span class="sxs-lookup"><span data-stu-id="05903-206">The value of a property is compared to a value in a set of value label pairs.</span></span> <span data-ttu-id="05903-207">Les paires d’étiquettes de valeur sont spécifiées dans le membre **lpSet** de l’Union de la structure.</span><span class="sxs-lookup"><span data-stu-id="05903-207">The value label pairs are specified in the **lpSet** member of the structure's union.</span></span> <br/> <span data-ttu-id="05903-208">Au moment de l’affichage, si la valeur de la propriété correspond à une valeur dans le jeu, une valeur et l’étiquette associée sont affichées.</span><span class="sxs-lookup"><span data-stu-id="05903-208">At display time, if the value of the property matches a value in the set, then both a value, and the associated label are displayed.</span></span><br/> |
| <span id="PROP_QUAL_LABELED_BITFIELD"></span><span id="prop_qual_labeled_bitfield"></span><dl> <span data-ttu-id="05903-209"><dt>**PROP \_ , \_ étiquette de champ de \_ champ**</dt></span><span class="sxs-lookup"><span data-stu-id="05903-209"><dt>**PROP\_QUAL\_LABELED\_BITFIELD**</dt></span></span> </dl> | <span data-ttu-id="05903-210">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="05903-210">Obsolete.</span></span> <span data-ttu-id="05903-211">Utilisez les indicateurs de compétences PROP à la \_ \_ place.</span><span class="sxs-lookup"><span data-stu-id="05903-211">Use PROP\_QUAL\_FLAGS instead.</span></span><br/>                                                                                                                                                                                                                                                                             |
| <span id="PROP_QUAL_CONST"></span><span id="prop_qual_const"></span><dl> <span data-ttu-id="05903-212"><dt>**PROP \_ Qualys \_ const**</dt></span><span class="sxs-lookup"><span data-stu-id="05903-212"><dt>**PROP\_QUAL\_CONST**</dt></span></span> </dl>                                   | <span data-ttu-id="05903-213">La valeur d’une propriété est comparée à une constante spécifiée dans le membre **value** de l’Union.</span><span class="sxs-lookup"><span data-stu-id="05903-213">The value of a property is compared to a constant that is specified in the **Value** member of the union.</span></span> <br/> <span data-ttu-id="05903-214">Au moment de l’affichage, si les valeurs de propriété et la constante ne correspondent pas, un message d’erreur mis en forme s’affiche avec la valeur définie sur normal.</span><span class="sxs-lookup"><span data-stu-id="05903-214">At display time, if the property values and constant do not match, a formatted error message appears with the value set as Normal.</span></span><br/>                                                             |
| <span id="PROP_QUAL_FLAGS"></span><span id="prop_qual_flags"></span><dl> <span data-ttu-id="05903-215"><dt>**indicateurs de compétences PROP \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="05903-215"><dt>**PROP\_QUAL\_FLAGS**</dt></span></span> </dl>                                   | <span data-ttu-id="05903-216">La valeur de la propriété est comparée aux BITs spécifiques identifiés dans le membre **lpSet** de l’Union.</span><span class="sxs-lookup"><span data-stu-id="05903-216">The value of the property is compared to specific BITs identified in the **lpSet** member of the union.</span></span><br/>                                                                                                                                                                                                              |
| <span id="PROP_QUAL_ARRAY"></span><span id="prop_qual_array"></span><dl> <span data-ttu-id="05903-217"><dt>**Tableau de compétences PROP \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="05903-217"><dt>**PROP\_QUAL\_ARRAY**</dt></span></span> </dl>                                   | <span data-ttu-id="05903-218">La valeur d’une propriété spécifie un tableau de valeurs.</span><span class="sxs-lookup"><span data-stu-id="05903-218">The value of a property specifies an array of values.</span></span> <span data-ttu-id="05903-219">La longueur des données attachées détermine la longueur d’un tableau.</span><span class="sxs-lookup"><span data-stu-id="05903-219">The length of attached data determines the length of an array.</span></span> <br/> <span data-ttu-id="05903-220">Lorsque la \_ valeur du tableau prop Qualys \_ est définie, le membre Union de la structure de données **PROPERTYINFO** a la valeur **null** et est ignoré.</span><span class="sxs-lookup"><span data-stu-id="05903-220">When the PROP\_QUAL\_ARRAY value is set, the union member of the **PROPERTYINFO** data structure is set to **NULL** and ignored.</span></span><br/>                                                    |



 

</dd> <dt>

<span data-ttu-id="05903-221">**lpExtendedInfo**</span><span class="sxs-lookup"><span data-stu-id="05903-221">**lpExtendedInfo**</span></span>
</dt> <dd>

<span data-ttu-id="05903-222">Réservé (membre de l’Union).</span><span class="sxs-lookup"><span data-stu-id="05903-222">Reserved (member of union).</span></span>

</dd> <dt>

<span data-ttu-id="05903-223">**lpRange**</span><span class="sxs-lookup"><span data-stu-id="05903-223">**lpRange**</span></span>
</dt> <dd>

<span data-ttu-id="05903-224">Pointeur vers une structure de [plage](range.md) qui définit une plage de valeurs.</span><span class="sxs-lookup"><span data-stu-id="05903-224">Pointer to a [RANGE](range.md) structure that defines a range of values.</span></span> <span data-ttu-id="05903-225">Ce membre doit être défini si le membre **DataQualifier** de cette structure a la valeur prop \_ Qualys \_ Range (membre de Union).</span><span class="sxs-lookup"><span data-stu-id="05903-225">This member must be set if the **DataQualifier** member of this structure is set to PROP\_QUAL\_RANGE (member of union).</span></span>

</dd> <dt>

<span data-ttu-id="05903-226">**lpSet**</span><span class="sxs-lookup"><span data-stu-id="05903-226">**lpSet**</span></span>
</dt> <dd>

<span data-ttu-id="05903-227">Pointeur vers une structure de [jeu](set.md) qui spécifie un ensemble de valeurs ou d’étiquettes.</span><span class="sxs-lookup"><span data-stu-id="05903-227">Pointer to a [SET](set.md) structure that specifies a set of values or labels.</span></span> <span data-ttu-id="05903-228">Ce membre doit être défini si le membre **DataQualifier** de la structure a la valeur prop \_ Qualys \_ Set, prop \_ Qualys \_ étiquetée \_ set ou prop \_ Qualys \_ Flags (member of Union).</span><span class="sxs-lookup"><span data-stu-id="05903-228">This member must be set if the **DataQualifier** member of the structure is set to PROP\_QUAL\_SET, PROP\_QUAL\_LABELED\_SET, or PROP\_QUAL\_FLAGS (member of union).</span></span>

</dd> <dt>

<span data-ttu-id="05903-229">**Binaire**</span><span class="sxs-lookup"><span data-stu-id="05903-229">**Bitmask**</span></span>
</dt> <dd>

<span data-ttu-id="05903-230">Obsolète (membre de l’Union).</span><span class="sxs-lookup"><span data-stu-id="05903-230">Obsolete (member of union).</span></span>

</dd> <dt>

<span data-ttu-id="05903-231">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="05903-231">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="05903-232">Valeur constante utilisée lorsque **DataQualifier** a la valeur prop \_ Qualys \_ const (membre de Union).</span><span class="sxs-lookup"><span data-stu-id="05903-232">Constant value used when the **DataQualifier** is set to PROP\_QUAL\_CONST (member of union).</span></span>

</dd> <dt>

<span data-ttu-id="05903-233">**FormatStringSize**</span><span class="sxs-lookup"><span data-stu-id="05903-233">**FormatStringSize**</span></span>
</dt> <dd>

<span data-ttu-id="05903-234">Taille maximale utilisée uniquement pour la description de la propriété.</span><span class="sxs-lookup"><span data-stu-id="05903-234">Maximum size used only for the property description.</span></span>

</dd> <dt>

<span data-ttu-id="05903-235">**InstanceData**</span><span class="sxs-lookup"><span data-stu-id="05903-235">**InstanceData**</span></span>
</dt> <dd>

<span data-ttu-id="05903-236">Spécifiez la fonction de format appelée pour mettre en forme les données affichées pour la propriété.</span><span class="sxs-lookup"><span data-stu-id="05903-236">Specify the format function that is called to format the displayed data for the property.</span></span> <span data-ttu-id="05903-237">Pour utiliser le formateur générique, spécifiez la fonction **FormatPropertyInstance** .</span><span class="sxs-lookup"><span data-stu-id="05903-237">To use the generic formatter, specify the **FormatPropertyInstance** function.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="05903-238">Notes</span><span class="sxs-lookup"><span data-stu-id="05903-238">Remarks</span></span>

<span data-ttu-id="05903-239">La structure **PROPERTYINFO** est utilisée dans les appels à la fonction [AddProperty](/previous-versions/bb251873(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="05903-239">The **PROPERTYINFO** structure is used in calls to the [AddProperty](/previous-versions/bb251873(v=msdn.10)) function.</span></span> <span data-ttu-id="05903-240">La fonction **AddProperty** ajoute une définition de propriété unique à la [*base de données des propriétés de*](p.md)l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="05903-240">The **AddProperty** function adds a single property definition to the parser [*property database*](p.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="05903-241">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="05903-241">Requirements</span></span>



| <span data-ttu-id="05903-242">Condition requise</span><span class="sxs-lookup"><span data-stu-id="05903-242">Requirement</span></span> | <span data-ttu-id="05903-243">Valeur</span><span class="sxs-lookup"><span data-stu-id="05903-243">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="05903-244">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05903-244">Minimum supported client</span></span><br/> | <span data-ttu-id="05903-245">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="05903-245">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="05903-246">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05903-246">Minimum supported server</span></span><br/> | <span data-ttu-id="05903-247">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="05903-247">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="05903-248">En-tête</span><span class="sxs-lookup"><span data-stu-id="05903-248">Header</span></span><br/>                   | <dl> <span data-ttu-id="05903-249"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="05903-249"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05903-250">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05903-250">See also</span></span>

<dl> <dt>

<span data-ttu-id="05903-251">[AddProperty](/previous-versions/bb251873(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="05903-251">[AddProperty](/previous-versions/bb251873(v=msdn.10))</span></span>
</dt> <dt>

[<span data-ttu-id="05903-252">RANGE</span><span class="sxs-lookup"><span data-stu-id="05903-252">RANGE</span></span>](range.md)
</dt> <dt>

[<span data-ttu-id="05903-253">SET</span><span class="sxs-lookup"><span data-stu-id="05903-253">SET</span></span>](set.md)
</dt> </dl>

 

