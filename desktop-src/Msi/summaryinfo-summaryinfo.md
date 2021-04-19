---
description: La propriété Property de l’objet SummaryInfo définit ou obtient la valeur de la propriété spécifiée dans le flux d’informations de résumé.
ms.assetid: 8e8f0987-c92b-43f3-a61a-35099188c629
title: Propriété SummaryInfo. Property
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SummaryInfo.Property
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 0e51773a930b8868e31a7e88848300a62b717912
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530499"
---
# <a name="summaryinfoproperty-property"></a><span data-ttu-id="ee9d8-103">Propriété SummaryInfo. Property</span><span class="sxs-lookup"><span data-stu-id="ee9d8-103">SummaryInfo.Property property</span></span>

<span data-ttu-id="ee9d8-104">La propriété **Property** de l’objet [**SummaryInfo**](summaryinfo-object.md) définit ou obtient la valeur de la propriété spécifiée dans le flux d’informations de résumé.</span><span class="sxs-lookup"><span data-stu-id="ee9d8-104">The **Property** property of the [**SummaryInfo**](summaryinfo-object.md) object sets or gets the value for the specified property in the summary information stream.</span></span> <span data-ttu-id="ee9d8-105">Les propriétés sont lues lorsque l’objet [**SummaryInfo**](summaryinfo-object.md) est créé, mais elles ne sont pas écrites tant que la méthode [**Persist**](summaryinfo-persist.md) n’est pas appelée.</span><span class="sxs-lookup"><span data-stu-id="ee9d8-105">The properties are read when the [**SummaryInfo**](summaryinfo-object.md) object is created, but they are not written until the [**Persist**](summaryinfo-persist.md) method is called.</span></span> <span data-ttu-id="ee9d8-106">La définition d’une propriété sur Empty entraîne sa suppression ; de même, la demande d’une propriété inexistante retourne une valeur vide.</span><span class="sxs-lookup"><span data-stu-id="ee9d8-106">Setting a property to Empty causes its removal; likewise, requesting a nonexistent property returns an Empty value.</span></span> <span data-ttu-id="ee9d8-107">Sinon, les valeurs peuvent être transférées comme des chaînes, des entiers ou des types date (date/heure).</span><span class="sxs-lookup"><span data-stu-id="ee9d8-107">Otherwise values may be transferred as strings, integers, or date (date time) types.</span></span>

<span data-ttu-id="ee9d8-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="ee9d8-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee9d8-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ee9d8-109">Syntax</span></span>


```JScript
propVal = SummaryInfo.Property
```



## <a name="property-value"></a><span data-ttu-id="ee9d8-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="ee9d8-110">Property value</span></span>

<span data-ttu-id="ee9d8-111">ID de propriété requis de l’une des propriétés de résumé.</span><span class="sxs-lookup"><span data-stu-id="ee9d8-111">Required property ID of one of the summary properties.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee9d8-112">Notes</span><span class="sxs-lookup"><span data-stu-id="ee9d8-112">Remarks</span></span>

<span data-ttu-id="ee9d8-113">**ID de propriété de résumé standard**</span><span class="sxs-lookup"><span data-stu-id="ee9d8-113">**Standard Summary Property IDs**</span></span>

<span data-ttu-id="ee9d8-114">(pas une énumération)</span><span class="sxs-lookup"><span data-stu-id="ee9d8-114">(not an enumeration)</span></span>



| <span data-ttu-id="ee9d8-115">Nom du paramètre</span><span class="sxs-lookup"><span data-stu-id="ee9d8-115">Parameter name</span></span>     | <span data-ttu-id="ee9d8-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee9d8-116">Value</span></span> | <span data-ttu-id="ee9d8-117">Description</span><span class="sxs-lookup"><span data-stu-id="ee9d8-117">Description</span></span>                                       |
|--------------------|-------|---------------------------------------------------|
| <span data-ttu-id="ee9d8-118">\_dictionnaire PID</span><span class="sxs-lookup"><span data-stu-id="ee9d8-118">PID\_DICTIONARY</span></span>    | <span data-ttu-id="ee9d8-119">0</span><span class="sxs-lookup"><span data-stu-id="ee9d8-119">0</span></span>     | <span data-ttu-id="ee9d8-120">Format spécial, non pris en charge par l’objet SummaryInfo</span><span class="sxs-lookup"><span data-stu-id="ee9d8-120">Special format, not support by SummaryInfo object</span></span> |
| <span data-ttu-id="ee9d8-121">\_page de codes PID</span><span class="sxs-lookup"><span data-stu-id="ee9d8-121">PID\_CODEPAGE</span></span>      | <span data-ttu-id="ee9d8-122">1</span><span class="sxs-lookup"><span data-stu-id="ee9d8-122">1</span></span>     | <span data-ttu-id="ee9d8-123">VT \_ I2</span><span class="sxs-lookup"><span data-stu-id="ee9d8-123">VT\_I2</span></span>                                            |
| <span data-ttu-id="ee9d8-124">\_titre PID</span><span class="sxs-lookup"><span data-stu-id="ee9d8-124">PID\_TITLE</span></span>         | <span data-ttu-id="ee9d8-125">2</span><span class="sxs-lookup"><span data-stu-id="ee9d8-125">2</span></span>     | <span data-ttu-id="ee9d8-126">VT- \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="ee9d8-126">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="ee9d8-127">\_objet PID</span><span class="sxs-lookup"><span data-stu-id="ee9d8-127">PID\_SUBJECT</span></span>       | <span data-ttu-id="ee9d8-128">3</span><span class="sxs-lookup"><span data-stu-id="ee9d8-128">3</span></span>     | <span data-ttu-id="ee9d8-129">VT- \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="ee9d8-129">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="ee9d8-130">\_auteur PID</span><span class="sxs-lookup"><span data-stu-id="ee9d8-130">PID\_AUTHOR</span></span>        | <span data-ttu-id="ee9d8-131">4</span><span class="sxs-lookup"><span data-stu-id="ee9d8-131">4</span></span>     | <span data-ttu-id="ee9d8-132">VT- \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="ee9d8-132">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="ee9d8-133">\_Mots clés PID</span><span class="sxs-lookup"><span data-stu-id="ee9d8-133">PID\_KEYWORDS</span></span>      | <span data-ttu-id="ee9d8-134">5</span><span class="sxs-lookup"><span data-stu-id="ee9d8-134">5</span></span>     | <span data-ttu-id="ee9d8-135">VT- \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="ee9d8-135">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="ee9d8-136">\_Commentaires PID</span><span class="sxs-lookup"><span data-stu-id="ee9d8-136">PID\_COMMENTS</span></span>      | <span data-ttu-id="ee9d8-137">6</span><span class="sxs-lookup"><span data-stu-id="ee9d8-137">6</span></span>     | <span data-ttu-id="ee9d8-138">VT- \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="ee9d8-138">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="ee9d8-139">\_modèle PID</span><span class="sxs-lookup"><span data-stu-id="ee9d8-139">PID\_TEMPLATE</span></span>      | <span data-ttu-id="ee9d8-140">7</span><span class="sxs-lookup"><span data-stu-id="ee9d8-140">7</span></span>     | <span data-ttu-id="ee9d8-141">VT- \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="ee9d8-141">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="ee9d8-142">PID \_ LASTAUTHOR</span><span class="sxs-lookup"><span data-stu-id="ee9d8-142">PID\_LASTAUTHOR</span></span>    | <span data-ttu-id="ee9d8-143">8</span><span class="sxs-lookup"><span data-stu-id="ee9d8-143">8</span></span>     | <span data-ttu-id="ee9d8-144">VT- \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="ee9d8-144">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="ee9d8-145">PID \_ REVNUMBER</span><span class="sxs-lookup"><span data-stu-id="ee9d8-145">PID\_REVNUMBER</span></span>     | <span data-ttu-id="ee9d8-146">9</span><span class="sxs-lookup"><span data-stu-id="ee9d8-146">9</span></span>     | <span data-ttu-id="ee9d8-147">VT- \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="ee9d8-147">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="ee9d8-148">PID \_ edittime</span><span class="sxs-lookup"><span data-stu-id="ee9d8-148">PID\_EDITTIME</span></span>      | <span data-ttu-id="ee9d8-149">10</span><span class="sxs-lookup"><span data-stu-id="ee9d8-149">10</span></span>    | <span data-ttu-id="ee9d8-150">de VT \_ fileTime</span><span class="sxs-lookup"><span data-stu-id="ee9d8-150">VT\_FILETIME</span></span>                                      |
| <span data-ttu-id="ee9d8-151">PID \_ LASTPRINTED</span><span class="sxs-lookup"><span data-stu-id="ee9d8-151">PID\_LASTPRINTED</span></span>   | <span data-ttu-id="ee9d8-152">11</span><span class="sxs-lookup"><span data-stu-id="ee9d8-152">11</span></span>    | <span data-ttu-id="ee9d8-153">de VT \_ fileTime</span><span class="sxs-lookup"><span data-stu-id="ee9d8-153">VT\_FILETIME</span></span>                                      |
| <span data-ttu-id="ee9d8-154">PID \_ créer \_ DTM</span><span class="sxs-lookup"><span data-stu-id="ee9d8-154">PID\_CREATE\_DTM</span></span>   | <span data-ttu-id="ee9d8-155">12</span><span class="sxs-lookup"><span data-stu-id="ee9d8-155">12</span></span>    | <span data-ttu-id="ee9d8-156">de VT \_ fileTime</span><span class="sxs-lookup"><span data-stu-id="ee9d8-156">VT\_FILETIME</span></span>                                      |
| <span data-ttu-id="ee9d8-157">PID \_ LASTSAVE \_ DTM</span><span class="sxs-lookup"><span data-stu-id="ee9d8-157">PID\_LASTSAVE\_DTM</span></span> | <span data-ttu-id="ee9d8-158">13</span><span class="sxs-lookup"><span data-stu-id="ee9d8-158">13</span></span>    | <span data-ttu-id="ee9d8-159">de VT \_ fileTime</span><span class="sxs-lookup"><span data-stu-id="ee9d8-159">VT\_FILETIME</span></span>                                      |
| <span data-ttu-id="ee9d8-160">PID \_ PageCount</span><span class="sxs-lookup"><span data-stu-id="ee9d8-160">PID\_PAGECOUNT</span></span>     | <span data-ttu-id="ee9d8-161">14</span><span class="sxs-lookup"><span data-stu-id="ee9d8-161">14</span></span>    | <span data-ttu-id="ee9d8-162">VT \_</span><span class="sxs-lookup"><span data-stu-id="ee9d8-162">VT\_I4</span></span>                                            |
| <span data-ttu-id="ee9d8-163">PID \_ WORDCOUNT</span><span class="sxs-lookup"><span data-stu-id="ee9d8-163">PID\_WORDCOUNT</span></span>     | <span data-ttu-id="ee9d8-164">15</span><span class="sxs-lookup"><span data-stu-id="ee9d8-164">15</span></span>    | <span data-ttu-id="ee9d8-165">VT \_</span><span class="sxs-lookup"><span data-stu-id="ee9d8-165">VT\_I4</span></span>                                            |
| <span data-ttu-id="ee9d8-166">ID de la PID \_</span><span class="sxs-lookup"><span data-stu-id="ee9d8-166">PID\_CHARCOUNT</span></span>     | <span data-ttu-id="ee9d8-167">16</span><span class="sxs-lookup"><span data-stu-id="ee9d8-167">16</span></span>    | <span data-ttu-id="ee9d8-168">VT \_</span><span class="sxs-lookup"><span data-stu-id="ee9d8-168">VT\_I4</span></span>                                            |
| <span data-ttu-id="ee9d8-169">\_miniature PID</span><span class="sxs-lookup"><span data-stu-id="ee9d8-169">PID\_THUMBNAIL</span></span>     | <span data-ttu-id="ee9d8-170">17</span><span class="sxs-lookup"><span data-stu-id="ee9d8-170">17</span></span>    | <span data-ttu-id="ee9d8-171">VT \_ CF (non pris en charge)</span><span class="sxs-lookup"><span data-stu-id="ee9d8-171">VT\_CF (not supported)</span></span>                            |
| <span data-ttu-id="ee9d8-172">PID \_ appname</span><span class="sxs-lookup"><span data-stu-id="ee9d8-172">PID\_APPNAME</span></span>       | <span data-ttu-id="ee9d8-173">18</span><span class="sxs-lookup"><span data-stu-id="ee9d8-173">18</span></span>    | <span data-ttu-id="ee9d8-174">VT- \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="ee9d8-174">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="ee9d8-175">\_sécurité PID</span><span class="sxs-lookup"><span data-stu-id="ee9d8-175">PID\_SECURITY</span></span>      | <span data-ttu-id="ee9d8-176">19</span><span class="sxs-lookup"><span data-stu-id="ee9d8-176">19</span></span>    | <span data-ttu-id="ee9d8-177">VT \_</span><span class="sxs-lookup"><span data-stu-id="ee9d8-177">VT\_I4</span></span>                                            |



 

<span data-ttu-id="ee9d8-178">**Types de données de propriété**</span><span class="sxs-lookup"><span data-stu-id="ee9d8-178">**Property Data Types**</span></span>

<span data-ttu-id="ee9d8-179">(pas une énumération)</span><span class="sxs-lookup"><span data-stu-id="ee9d8-179">(not an enumeration)</span></span>



| <span data-ttu-id="ee9d8-180">Nom du paramètre</span><span class="sxs-lookup"><span data-stu-id="ee9d8-180">Parameter name</span></span> | <span data-ttu-id="ee9d8-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee9d8-181">Value</span></span> | <span data-ttu-id="ee9d8-182">Description</span><span class="sxs-lookup"><span data-stu-id="ee9d8-182">Description</span></span>                                                                              |
|----------------|-------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee9d8-183">VT \_ I2</span><span class="sxs-lookup"><span data-stu-id="ee9d8-183">VT\_I2</span></span>         | <span data-ttu-id="ee9d8-184">2</span><span class="sxs-lookup"><span data-stu-id="ee9d8-184">2</span></span>     | <span data-ttu-id="ee9d8-185">Entier de 16 bits</span><span class="sxs-lookup"><span data-stu-id="ee9d8-185">16-bit integer</span></span>                                                                           |
| <span data-ttu-id="ee9d8-186">VT \_</span><span class="sxs-lookup"><span data-stu-id="ee9d8-186">VT\_I4</span></span>         | <span data-ttu-id="ee9d8-187">3</span><span class="sxs-lookup"><span data-stu-id="ee9d8-187">3</span></span>     | <span data-ttu-id="ee9d8-188">Entier de 32 bits</span><span class="sxs-lookup"><span data-stu-id="ee9d8-188">32-bit integer</span></span>                                                                           |
| <span data-ttu-id="ee9d8-189">VT- \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="ee9d8-189">VT\_LPSTR</span></span>      | <span data-ttu-id="ee9d8-190">30</span><span class="sxs-lookup"><span data-stu-id="ee9d8-190">30</span></span>    | <span data-ttu-id="ee9d8-191">String</span><span class="sxs-lookup"><span data-stu-id="ee9d8-191">String</span></span>                                                                                   |
| <span data-ttu-id="ee9d8-192">de VT \_ fileTime</span><span class="sxs-lookup"><span data-stu-id="ee9d8-192">VT\_FILETIME</span></span>   | <span data-ttu-id="ee9d8-193">64</span><span class="sxs-lookup"><span data-stu-id="ee9d8-193">64</span></span>    | <span data-ttu-id="ee9d8-194">Date et heure (FILETIME, converties en heure variant)</span><span class="sxs-lookup"><span data-stu-id="ee9d8-194">Date time (FILETIME, converted to Variant time)</span></span>                                          |
| <span data-ttu-id="ee9d8-195">\_CF VT</span><span class="sxs-lookup"><span data-stu-id="ee9d8-195">VT\_CF</span></span>         | <span data-ttu-id="ee9d8-196">71</span><span class="sxs-lookup"><span data-stu-id="ee9d8-196">71</span></span>    | <span data-ttu-id="ee9d8-197">Format du presse-papiers + données, non géré par l’objet [**SummaryInfo**](summaryinfo-object.md)</span><span class="sxs-lookup"><span data-stu-id="ee9d8-197">Clipboard format + data, not handled by [**SummaryInfo**](summaryinfo-object.md) object</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="ee9d8-198">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ee9d8-198">Requirements</span></span>



| <span data-ttu-id="ee9d8-199">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ee9d8-199">Requirement</span></span> | <span data-ttu-id="ee9d8-200">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee9d8-200">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee9d8-201">Version</span><span class="sxs-lookup"><span data-stu-id="ee9d8-201">Version</span></span><br/> | <span data-ttu-id="ee9d8-202">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ee9d8-202">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ee9d8-203">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ee9d8-203">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ee9d8-204">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="ee9d8-204">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="ee9d8-205">DLL</span><span class="sxs-lookup"><span data-stu-id="ee9d8-205">DLL</span></span><br/>     | <dl> <span data-ttu-id="ee9d8-206"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee9d8-206"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="ee9d8-207">IID</span><span class="sxs-lookup"><span data-stu-id="ee9d8-207">IID</span></span><br/>     | <span data-ttu-id="ee9d8-208">IID \_ ISummaryInfo est défini en tant que 000C109B-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="ee9d8-208">IID\_ISummaryInfo is defined as 000C109B-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="ee9d8-209">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee9d8-209">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee9d8-210">**MsiSummaryInfoSetProperty**</span><span class="sxs-lookup"><span data-stu-id="ee9d8-210">**MsiSummaryInfoSetProperty**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfosetpropertya)
</dt> <dt>

[<span data-ttu-id="ee9d8-211">**MsiSummaryInfoGetProperty**</span><span class="sxs-lookup"><span data-stu-id="ee9d8-211">**MsiSummaryInfoGetProperty**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertya)
</dt> </dl>

 

 




