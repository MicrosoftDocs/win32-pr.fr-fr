---
description: La fonction EnumPrinters énumère les imprimantes disponibles, les serveurs d’impression, les domaines ou les fournisseurs d’impression.
ms.assetid: 0d0cc726-c515-4146-9273-cdf1db3c76b7
title: EnumPrinters, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinters
- EnumPrintersA
- EnumPrintersW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 6d82e8e6ff4f56a3c67fa29c48e982ebe0fd4599
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864970"
---
# <a name="enumprinters-function"></a><span data-ttu-id="61e3f-103">EnumPrinters fonction)</span><span class="sxs-lookup"><span data-stu-id="61e3f-103">EnumPrinters function</span></span>

<span data-ttu-id="61e3f-104">La fonction **EnumPrinters** énumère les imprimantes disponibles, les serveurs d’impression, les domaines ou les fournisseurs d’impression.</span><span class="sxs-lookup"><span data-stu-id="61e3f-104">The **EnumPrinters** function enumerates available printers, print servers, domains, or print providers.</span></span>

## <a name="syntax"></a><span data-ttu-id="61e3f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="61e3f-105">Syntax</span></span>


```C++
BOOL EnumPrinters(
  _In_  DWORD   Flags,
  _In_  LPTSTR  Name,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPrinterEnum,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="61e3f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="61e3f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61e3f-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="61e3f-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61e3f-108">Types d’objets d’impression que la fonction doit énumérer.</span><span class="sxs-lookup"><span data-stu-id="61e3f-108">The types of print objects that the function should enumerate.</span></span> <span data-ttu-id="61e3f-109">Cette valeur peut être une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="61e3f-109">This value can be one or more of the following values.</span></span>



| <span data-ttu-id="61e3f-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="61e3f-110">Value</span></span>                                                                                                                                                                                               | <span data-ttu-id="61e3f-111">Signification</span><span class="sxs-lookup"><span data-stu-id="61e3f-111">Meaning</span></span>                                                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRINTER_ENUM_LOCAL"></span><span id="printer_enum_local"></span><dl> <span data-ttu-id="61e3f-112"><dt>**\_enum \_ local de l’imprimante**</dt></span><span class="sxs-lookup"><span data-stu-id="61e3f-112"><dt>**PRINTER\_ENUM\_LOCAL**</dt></span></span> </dl>                       | <span data-ttu-id="61e3f-113">Si l’indicateur de nom d’enum d’imprimante \_ \_ n’est pas également passé, la fonction ignore le paramètre *Name* et énumère les imprimantes installées localement.</span><span class="sxs-lookup"><span data-stu-id="61e3f-113">If the PRINTER\_ENUM\_NAME flag is not also passed, the function ignores the *Name* parameter, and enumerates the locally installed printers.</span></span> <span data-ttu-id="61e3f-114">Si \_ \_ le nom d’enum de l’imprimante est également passé, la fonction énumère les imprimantes locales sur le *nom*.</span><span class="sxs-lookup"><span data-stu-id="61e3f-114">If PRINTER\_ENUM\_NAME is also passed, the function enumerates the local printers on *Name*.</span></span> <br/> |
| <span id="PRINTER_ENUM_NAME"></span><span id="printer_enum_name"></span><dl> <span data-ttu-id="61e3f-115"><dt>**nom de l’enum de l’imprimante \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="61e3f-115"><dt>**PRINTER\_ENUM\_NAME**</dt></span></span> </dl>                          | <span data-ttu-id="61e3f-116">La fonction énumère l’imprimante identifiée par son *nom*.</span><span class="sxs-lookup"><span data-stu-id="61e3f-116">The function enumerates the printer identified by *Name*.</span></span> <span data-ttu-id="61e3f-117">Il peut s’agir d’un serveur, d’un domaine ou d’un fournisseur d’impression.</span><span class="sxs-lookup"><span data-stu-id="61e3f-117">This can be a server, a domain, or a print provider.</span></span> <span data-ttu-id="61e3f-118">Si le *nom* est **null**, la fonction énumère les fournisseurs d’impression disponibles.</span><span class="sxs-lookup"><span data-stu-id="61e3f-118">If *Name* is **NULL**, the function enumerates available print providers.</span></span><br/>                                                    |
| <span id="PRINTER_ENUM_SHARED"></span><span id="printer_enum_shared"></span><dl> <span data-ttu-id="61e3f-119"><dt>**ENUM d’imprimante \_ \_ partagé**</dt></span><span class="sxs-lookup"><span data-stu-id="61e3f-119"><dt>**PRINTER\_ENUM\_SHARED**</dt></span></span> </dl>                    | <span data-ttu-id="61e3f-120">La fonction énumère les imprimantes qui ont l’attribut Shared.</span><span class="sxs-lookup"><span data-stu-id="61e3f-120">The function enumerates printers that have the shared attribute.</span></span> <span data-ttu-id="61e3f-121">Ne peut pas être utilisé de manière isolée ; Utilisez une opération ou pour combiner avec un autre \_ type d’énumération d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="61e3f-121">Cannot be used in isolation; use an OR operation to combine with another PRINTER\_ENUM type.</span></span><br/>                                                                               |
| <span id="PRINTER_ENUM_CONNECTIONS"></span><span id="printer_enum_connections"></span><dl> <span data-ttu-id="61e3f-122"><dt>**\_connexions d’énumération d’imprimantes \_**</dt></span><span class="sxs-lookup"><span data-stu-id="61e3f-122"><dt>**PRINTER\_ENUM\_CONNECTIONS**</dt></span></span> </dl>     | <span data-ttu-id="61e3f-123">La fonction énumère la liste des imprimantes auxquelles l’utilisateur a effectué des connexions précédentes.</span><span class="sxs-lookup"><span data-stu-id="61e3f-123">The function enumerates the list of printers to which the user has made previous connections.</span></span><br/>                                                                                                                                               |
| <span id="PRINTER_ENUM_NETWORK"></span><span id="printer_enum_network"></span><dl> <span data-ttu-id="61e3f-124"><dt>**\_réseau d’énumération d’imprimantes \_**</dt></span><span class="sxs-lookup"><span data-stu-id="61e3f-124"><dt>**PRINTER\_ENUM\_NETWORK**</dt></span></span> </dl>                 | <span data-ttu-id="61e3f-125">La fonction énumère les imprimantes réseau dans le domaine de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="61e3f-125">The function enumerates network printers in the computer's domain.</span></span> <span data-ttu-id="61e3f-126">Cette valeur est valide uniquement si *Level* a la valeur 1.</span><span class="sxs-lookup"><span data-stu-id="61e3f-126">This value is valid only if *Level* is 1.</span></span><br/>                                                                                                                                |
| <span id="PRINTER_ENUM_REMOTE"></span><span id="printer_enum_remote"></span><dl> <span data-ttu-id="61e3f-127"><dt>**IMPRIMANTE \_ \_ à distance enum**</dt></span><span class="sxs-lookup"><span data-stu-id="61e3f-127"><dt>**PRINTER\_ENUM\_REMOTE**</dt></span></span> </dl>                    | <span data-ttu-id="61e3f-128">La fonction énumère les imprimantes réseau et les serveurs d’impression dans le domaine de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="61e3f-128">The function enumerates network printers and print servers in the computer's domain.</span></span> <span data-ttu-id="61e3f-129">Cette valeur est valide uniquement si *Level* a la valeur 1.</span><span class="sxs-lookup"><span data-stu-id="61e3f-129">This value is valid only if *Level* is 1.</span></span><br/>                                                                                                              |
| <span id="PRINTER_ENUM_CATEGORY_3D"></span><span id="printer_enum_category_3d"></span><dl> <span data-ttu-id="61e3f-130"><dt>**\_Catégorie d’énumération d’imprimantes \_ \_ 3D**</dt></span><span class="sxs-lookup"><span data-stu-id="61e3f-130"><dt>**PRINTER\_ENUM\_CATEGORY\_3D**</dt></span></span> </dl>    | <span data-ttu-id="61e3f-131">La fonction énumère uniquement les imprimantes 3D.</span><span class="sxs-lookup"><span data-stu-id="61e3f-131">The function enumerates only 3D printers.</span></span><br/>                                                                                                                                                                                                   |
| <span id="PRINTER_ENUM_CATEGORY_ALL"></span><span id="printer_enum_category_all"></span><dl> <span data-ttu-id="61e3f-132"><dt>**IMPRIMANTE \_ \_ catégorie \_ tout**</dt></span><span class="sxs-lookup"><span data-stu-id="61e3f-132"><dt>**PRINTER\_ENUM\_CATEGORY\_ALL**</dt></span></span> </dl> | <span data-ttu-id="61e3f-133">La fonction énumère tous les périphériques d’impression, y compris les imprimantes 3D.</span><span class="sxs-lookup"><span data-stu-id="61e3f-133">The function enumerates all print devices, including 3D printers.</span></span><br/>                                                                                                                                                                           |



 

<span data-ttu-id="61e3f-134">Si le *niveau* est 4, vous ne pouvez utiliser que les \_ connexions d’énumération d’imprimante et les \_ \_ \_ constantes d’imprimante locales Enum.</span><span class="sxs-lookup"><span data-stu-id="61e3f-134">If *Level* is 4, you can only use the PRINTER\_ENUM\_CONNECTIONS and PRINTER\_ENUM\_LOCAL constants.</span></span>

> [!Note]  
> <span data-ttu-id="61e3f-135">les périphériques d’impression 3D ne sont pas énumérés par défaut.</span><span class="sxs-lookup"><span data-stu-id="61e3f-135">3D print devices are not enumerated by default.</span></span> <span data-ttu-id="61e3f-136">Vous devez inclure à la fois **Printer \_ enum \_ Category \_ 3D** et **Printer \_ enum \_ local** pour énumérer uniquement les imprimantes 3D.</span><span class="sxs-lookup"><span data-stu-id="61e3f-136">You must include both **PRINTER\_ENUM\_CATEGORY\_3D** and **PRINTER\_ENUM\_LOCAL** to enumerate only 3D printers.</span></span> <span data-ttu-id="61e3f-137">Pour inclure des imprimantes 3D, ainsi que toutes les autres imprimantes locales, utilisez l' **\_ énumération d’imprimante \_ catégorie \_ tout** et l' **\_ énumération \_ locale** de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="61e3f-137">To include 3D printers, along with all other local printers, use **PRINTER\_ENUM\_CATEGORY\_ALL** and **PRINTER\_ENUM\_LOCAL**.</span></span>

 

</dd> <dt>

<span data-ttu-id="61e3f-138">*Nom* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="61e3f-138">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61e3f-139">Si *Level* a la valeur 1, *Flags* contient le nom de l’enum d’imprimante \_ et le \_ *nom* n’est pas **null**, le *nom* est un pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom de l’objet à énumérer.</span><span class="sxs-lookup"><span data-stu-id="61e3f-139">If *Level* is 1, *Flags* contains PRINTER\_ENUM\_NAME, and *Name* is non-**NULL**, then *Name* is a pointer to a null-terminated string that specifies the name of the object to enumerate.</span></span> <span data-ttu-id="61e3f-140">Cette chaîne peut être le nom d’un serveur, d’un domaine ou d’un fournisseur d’impression.</span><span class="sxs-lookup"><span data-stu-id="61e3f-140">This string can be the name of a server, a domain, or a print provider.</span></span>

<span data-ttu-id="61e3f-141">Si *Level* a la valeur 1, *Flags* contient le nom de l’enum d’imprimante \_ \_ et *Name* est **null**, puis la fonction énumère les fournisseurs d’impression disponibles.</span><span class="sxs-lookup"><span data-stu-id="61e3f-141">If *Level* is 1, *Flags* contains PRINTER\_ENUM\_NAME, and *Name* is **NULL**, then the function enumerates the available print providers.</span></span>

<span data-ttu-id="61e3f-142">Si *Level* a la valeur 1, *Flags* contient Printer \_ enum \_ Remote et *Name* est **null**, alors que la fonction énumère les imprimantes dans le domaine de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="61e3f-142">If *Level* is 1, *Flags* contains PRINTER\_ENUM\_REMOTE, and *Name* is **NULL**, then the function enumerates the printers in the user's domain.</span></span>

<span data-ttu-id="61e3f-143">Si *Level* a la valeur 2 ou 5,*Name* est un pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom d’un serveur dont les imprimantes doivent être énumérées.</span><span class="sxs-lookup"><span data-stu-id="61e3f-143">If *Level* is 2 or 5,*Name* is a pointer to a null-terminated string that specifies the name of a server whose printers are to be enumerated.</span></span> <span data-ttu-id="61e3f-144">Si cette chaîne est **null**, la fonction énumère les imprimantes installées sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="61e3f-144">If this string is **NULL**, then the function enumerates the printers installed on the local computer.</span></span>

<span data-ttu-id="61e3f-145">Si le *niveau* est 4, le *nom* doit être **null**.</span><span class="sxs-lookup"><span data-stu-id="61e3f-145">If *Level* is 4, *Name* should be **NULL**.</span></span> <span data-ttu-id="61e3f-146">La fonction interroge toujours sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="61e3f-146">The function always queries on the local computer.</span></span>

<span data-ttu-id="61e3f-147">Quand *Name* a la **valeur null**, la définition d' *indicateurs* sur Printer Printer \_ \_ local \| Printer \_ \_ connections énumère les imprimantes installées sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="61e3f-147">When *Name* is **NULL**, setting *Flags* to PRINTER\_ENUM\_LOCAL \| PRINTER\_ENUM\_CONNECTIONS enumerates printers that are installed on the local machine.</span></span> <span data-ttu-id="61e3f-148">Ces imprimantes incluent celles qui sont physiquement connectées à l’ordinateur local, ainsi que les imprimantes distantes sur lesquelles il dispose d’une connexion réseau.</span><span class="sxs-lookup"><span data-stu-id="61e3f-148">These printers include those that are physically attached to the local machine as well as remote printers to which it has a network connection.</span></span>

<span data-ttu-id="61e3f-149">Si le *nom* n’est pas **null**, la définition des *indicateurs* sur Printer nom enum de l' \_ \_ \| imprimante locale \_ \_ énumère les imprimantes locales qui sont installées sur le *nom* du serveur.</span><span class="sxs-lookup"><span data-stu-id="61e3f-149">When *Name* is not **NULL**, setting *Flags* to PRINTER\_ENUM\_LOCAL \| PRINTER\_ENUM\_NAME enumerates the local printers that are installed on the server *Name*.</span></span>

</dd> <dt>

<span data-ttu-id="61e3f-150">De *niveau* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="61e3f-150">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61e3f-151">Type des structures de données vers lesquelles pointe *pPrinterEnum*.</span><span class="sxs-lookup"><span data-stu-id="61e3f-151">The type of data structures pointed to by *pPrinterEnum*.</span></span> <span data-ttu-id="61e3f-152">Les valeurs valides sont 1, 2, 4 et 5, qui correspondent aux structures de données [**Printer \_ info \_ 1**](printer-info-1.md), [**Printer \_ info \_ 2**](printer-info-2.md) , [**Printer \_ info \_ 4**](printer-info-4.md)et [**Printer \_ info \_ 5**](printer-info-5.md) .</span><span class="sxs-lookup"><span data-stu-id="61e3f-152">Valid values are 1, 2, 4, and 5, which correspond to the [**PRINTER\_INFO\_1**](printer-info-1.md), [**PRINTER\_INFO\_2**](printer-info-2.md) , [**PRINTER\_INFO\_4**](printer-info-4.md), and [**PRINTER\_INFO\_5**](printer-info-5.md) data structures.</span></span>

<span data-ttu-id="61e3f-153">Cette valeur peut être 1, 2, 4 ou 5.</span><span class="sxs-lookup"><span data-stu-id="61e3f-153">This value can be 1, 2, 4, or 5.</span></span>

</dd> <dt>

<span data-ttu-id="61e3f-154">*pPrinterEnum* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="61e3f-154">*pPrinterEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="61e3f-155">Pointeur vers une mémoire tampon qui reçoit un tableau de structures d' [**informations d’imprimante \_ \_ 1**](printer-info-1.md), d’informations d’imprimante [**\_ \_ 2**](printer-info-2.md), d' [**informations d’imprimante \_ \_ 4**](printer-info-4.md)ou d' [**informations d’imprimante \_ \_ 5**](printer-info-5.md) .</span><span class="sxs-lookup"><span data-stu-id="61e3f-155">A pointer to a buffer that receives an array of [**PRINTER\_INFO\_1**](printer-info-1.md), [**PRINTER\_INFO\_2**](printer-info-2.md), [**PRINTER\_INFO\_4**](printer-info-4.md), or [**PRINTER\_INFO\_5**](printer-info-5.md) structures.</span></span> <span data-ttu-id="61e3f-156">Chaque structure contient des données qui décrivent un objet d’impression disponible.</span><span class="sxs-lookup"><span data-stu-id="61e3f-156">Each structure contains data that describes an available print object.</span></span>

<span data-ttu-id="61e3f-157">Si le *niveau* est 1, le tableau contient les structures des [**informations d’imprimante \_ \_ 1**](printer-info-1.md) .</span><span class="sxs-lookup"><span data-stu-id="61e3f-157">If *Level* is 1, the array contains [**PRINTER\_INFO\_1**](printer-info-1.md) structures.</span></span> <span data-ttu-id="61e3f-158">Si le *niveau* est 2, le tableau contient les structures des [**informations d’imprimante \_ \_ 2**](printer-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="61e3f-158">If *Level* is 2, the array contains [**PRINTER\_INFO\_2**](printer-info-2.md) structures.</span></span> <span data-ttu-id="61e3f-159">Si le *niveau* est 4, le tableau contient les structures de l' [**imprimante \_ info \_ 4**](printer-info-4.md) .</span><span class="sxs-lookup"><span data-stu-id="61e3f-159">If *Level* is 4, the array contains [**PRINTER\_INFO\_4**](printer-info-4.md) structures.</span></span> <span data-ttu-id="61e3f-160">Si le *niveau* est 5, le tableau contient les structures des [**informations d’imprimante \_ \_ 5**](printer-info-5.md) .</span><span class="sxs-lookup"><span data-stu-id="61e3f-160">If *Level* is 5, the array contains [**PRINTER\_INFO\_5**](printer-info-5.md) structures.</span></span>

<span data-ttu-id="61e3f-161">La mémoire tampon doit être suffisamment grande pour recevoir le tableau de structures de données et toutes les chaînes ou autres données auxquelles les membres de la structure pointent.</span><span class="sxs-lookup"><span data-stu-id="61e3f-161">The buffer must be large enough to receive the array of data structures and any strings or other data to which the structure members point.</span></span> <span data-ttu-id="61e3f-162">Si la mémoire tampon est trop petite, le paramètre *pcbNeeded* retourne la taille de mémoire tampon requise.</span><span class="sxs-lookup"><span data-stu-id="61e3f-162">If the buffer is too small, the *pcbNeeded* parameter returns the required buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="61e3f-163">*cbBuf* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="61e3f-163">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61e3f-164">Taille, en octets, de la mémoire tampon vers laquelle pointe *pPrinterEnum*.</span><span class="sxs-lookup"><span data-stu-id="61e3f-164">The size, in bytes, of the buffer pointed to by *pPrinterEnum*.</span></span>

</dd> <dt>

<span data-ttu-id="61e3f-165">*pcbNeeded* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="61e3f-165">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="61e3f-166">Pointeur vers une valeur qui reçoit le nombre d’octets copiés si la fonction est réussie ou le nombre d’octets requis si *cbBuf* est trop petit.</span><span class="sxs-lookup"><span data-stu-id="61e3f-166">A pointer to a value that receives the number of bytes copied if the function succeeds or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> <dt>

<span data-ttu-id="61e3f-167">*pcReturned* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="61e3f-167">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="61e3f-168">Pointeur vers une valeur qui reçoit le nombre de structures [**Printer \_ info \_ 1**](printer-info-1.md), [**Printer \_ info \_ 2**](printer-info-2.md) , [**Printer \_ info \_ 4**](printer-info-4.md)ou [**Printer \_ info \_ 5**](printer-info-5.md) que la fonction retourne dans le tableau auquel *pPrinterEnum* pointe.</span><span class="sxs-lookup"><span data-stu-id="61e3f-168">A pointer to a value that receives the number of [**PRINTER\_INFO\_1**](printer-info-1.md), [**PRINTER\_INFO\_2**](printer-info-2.md) , [**PRINTER\_INFO\_4**](printer-info-4.md), or [**PRINTER\_INFO\_5**](printer-info-5.md) structures that the function returns in the array to which *pPrinterEnum* points.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61e3f-169">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="61e3f-169">Return value</span></span>

<span data-ttu-id="61e3f-170">Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="61e3f-170">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="61e3f-171">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="61e3f-171">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="61e3f-172">Notes</span><span class="sxs-lookup"><span data-stu-id="61e3f-172">Remarks</span></span>

<span data-ttu-id="61e3f-173">N’appelez pas cette méthode dans [**DllMain**](/windows/desktop/Dlls/dllmain).</span><span class="sxs-lookup"><span data-stu-id="61e3f-173">Do not call this method in [**DllMain**](/windows/desktop/Dlls/dllmain).</span></span>

> [!Note]  
> <span data-ttu-id="61e3f-174">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="61e3f-174">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="61e3f-175">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="61e3f-175">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="61e3f-176">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="61e3f-176">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="61e3f-177">Si **EnumPrinters** retourne une structure d' [**informations d’imprimante \_ \_ 1**](printer-info-1.md) dans laquelle le \_ conteneur d’énumération d’imprimante \_ est spécifié, cela indique qu’il existe une hiérarchie d’objets Printer.</span><span class="sxs-lookup"><span data-stu-id="61e3f-177">If **EnumPrinters** returns a [**PRINTER\_INFO\_1**](printer-info-1.md) structure in which PRINTER\_ENUM\_CONTAINER is specified, this indicates that there is a hierarchy of printer objects.</span></span> <span data-ttu-id="61e3f-178">Une application peut énumérer la hiérarchie en appelant à nouveau **EnumPrinters** , en affectant à *Name* la valeur du membre **pname** de la structure **\_ info \_ 1** de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="61e3f-178">An application can enumerate the hierarchy by calling **EnumPrinters** again, setting *Name* to the value of the **PRINTER\_INFO\_1** structure's **pName** member.</span></span>

<span data-ttu-id="61e3f-179">La fonction **EnumPrinters** ne récupère pas les informations de sécurité.</span><span class="sxs-lookup"><span data-stu-id="61e3f-179">The **EnumPrinters** function does not retrieve security information.</span></span> <span data-ttu-id="61e3f-180">Si les structures [**\_ info \_ 2**](printer-info-2.md) de l’imprimante sont retournées dans le tableau pointé par *pPrinterEnum*, leurs membres *pSecurityDescriptor* seront définis sur **null**.</span><span class="sxs-lookup"><span data-stu-id="61e3f-180">If [**PRINTER\_INFO\_2**](printer-info-2.md) structures are returned in the array pointed to by *pPrinterEnum*, their *pSecurityDescriptor* members will be set to **NULL**.</span></span>

<span data-ttu-id="61e3f-181">Pour obtenir des informations sur l’imprimante par défaut, appelez [**GetDefaultPrinter**](getdefaultprinter.md).</span><span class="sxs-lookup"><span data-stu-id="61e3f-181">To get information about the default printer, call [**GetDefaultPrinter**](getdefaultprinter.md).</span></span>

<span data-ttu-id="61e3f-182">La structure [**Printer \_ info \_ 4**](printer-info-4.md) offre un moyen simple et extrêmement rapide de récupérer les noms des imprimantes installées sur un ordinateur local, ainsi que les connexions distantes qu’un utilisateur a établies.</span><span class="sxs-lookup"><span data-stu-id="61e3f-182">The [**PRINTER\_INFO\_4**](printer-info-4.md) structure provides an easy and extremely fast way to retrieve the names of the printers installed on a local machine, as well as the remote connections that a user has established.</span></span> <span data-ttu-id="61e3f-183">Quand **EnumPrinters** est appelé avec une structure de données **Printer \_ info \_ 4** , cette fonction interroge le registre pour obtenir les informations spécifiées, puis retourne immédiatement.</span><span class="sxs-lookup"><span data-stu-id="61e3f-183">When **EnumPrinters** is called with a **PRINTER\_INFO\_4** data structure, that function queries the registry for the specified information, then returns immediately.</span></span> <span data-ttu-id="61e3f-184">Cela diffère du comportement de **EnumPrinters** lorsqu’il est appelé avec d’autres niveaux de **structures de données d' \_ informations sur l’imprimante \_ \* *. En particulier, lorsque _* EnumPrinters** est appelé avec une structure de données de niveau 2 ([**Printer \_ info \_ 2**](printer-info-2.md)), il effectue un appel [**OpenPrinter**](openprinter.md) sur chaque connexion à distance.</span><span class="sxs-lookup"><span data-stu-id="61e3f-184">This differs from the behavior of **EnumPrinters** when called with other levels of **PRINTER\_INFO\_\**_ data structures. In particular, when _\* EnumPrinters*\* is called with a level 2 ([**PRINTER\_INFO\_2**](printer-info-2.md)) data structure, it performs an [**OpenPrinter**](openprinter.md) call on each remote connection.</span></span> <span data-ttu-id="61e3f-185">Si une connexion distante est interrompue ou si le serveur distant n’existe plus, ou si l’imprimante distante n’existe plus, la fonction doit attendre que RPC expire et, par conséquent, faire échouer l’appel **OpenPrinter** .</span><span class="sxs-lookup"><span data-stu-id="61e3f-185">If a remote connection is down, or the remote server no longer exists, or the remote printer no longer exists, the function must wait for RPC to time out and consequently fail the **OpenPrinter** call.</span></span> <span data-ttu-id="61e3f-186">Cette opération peut prendre du temps.</span><span class="sxs-lookup"><span data-stu-id="61e3f-186">This can take a while.</span></span> <span data-ttu-id="61e3f-187">Le passage d’une structure **Printer \_ info \_ 4** permet à une application de récupérer un minimum d’informations requises ; si des informations plus détaillées sont souhaitées, un appel **EnumPrinters** de niveau 2 suivant peut être effectué.</span><span class="sxs-lookup"><span data-stu-id="61e3f-187">Passing a **PRINTER\_INFO\_4** structure lets an application retrieve a bare minimum of required information; if more detailed information is desired, a subsequent **EnumPrinters** level 2 call can be made.</span></span>

<span data-ttu-id="61e3f-188">**Windows Vista :** Les données d’imprimante retournées par **EnumPrinters** sont extraites d’un cache local lorsque la valeur de *Level* est 4.</span><span class="sxs-lookup"><span data-stu-id="61e3f-188">**Windows Vista:** The printer data returned by **EnumPrinters** is retrieved from a local cache when the value of *Level* is 4.</span></span>

<span data-ttu-id="61e3f-189">Le tableau suivant montre la sortie **EnumPrinters** pour les différentes valeurs d' *indicateurs* lorsque le paramètre de *niveau* a la valeur 1.</span><span class="sxs-lookup"><span data-stu-id="61e3f-189">The following table shows the **EnumPrinters** output for various *Flags* values when the *Level* parameter is set to 1.</span></span>

<span data-ttu-id="61e3f-190">Dans la colonne paramètre de *nom* de la table, vous devez remplacer un nom approprié pour le fournisseur d’impression, le domaine et l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="61e3f-190">In the *Name* parameter column of the table, you should substitute an appropriate name for Print Provider, Domain, and Machine.</span></span> <span data-ttu-id="61e3f-191">Par exemple, pour « fournisseur d’impression », vous pouvez utiliser le nom du fournisseur d’impression réseau ou le nom du fournisseur d’impression local.</span><span class="sxs-lookup"><span data-stu-id="61e3f-191">For example, for "Print Provider," you could use the name of the network print provider or the name of the local print provider.</span></span> <span data-ttu-id="61e3f-192">Pour récupérer les noms des fournisseurs d’impression, appelez **EnumPrinters** avec le *nom* défini sur **null**.</span><span class="sxs-lookup"><span data-stu-id="61e3f-192">To retrieve print provider names, call **EnumPrinters** with *Name* set to **NULL**.</span></span>



| <span data-ttu-id="61e3f-193">Paramètre *Flags*</span><span class="sxs-lookup"><span data-stu-id="61e3f-193">*Flags* parameter</span></span>                                  | <span data-ttu-id="61e3f-194">Paramètre *Name*</span><span class="sxs-lookup"><span data-stu-id="61e3f-194">*Name* parameter</span></span>                            | <span data-ttu-id="61e3f-195">Résultats</span><span class="sxs-lookup"><span data-stu-id="61e3f-195">Result</span></span>                                                                                            |
|----------------------------------------------------|---------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61e3f-196">PRINTER \_ \_ local enum local (et non pas le nom enum de l’imprimante \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="61e3f-196">PRINTER\_ENUM\_LOCAL (and not PRINTER\_ENUM\_NAME)</span></span> | <span data-ttu-id="61e3f-197">Le paramètre *Name* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="61e3f-197">The *Name* parameter is ignored.</span></span><br/> | <span data-ttu-id="61e3f-198">Toutes les imprimantes locales.</span><span class="sxs-lookup"><span data-stu-id="61e3f-198">All local printers.</span></span><br/>                                                                    |
| <span data-ttu-id="61e3f-199">nom de l’enum de l’imprimante \_ \_</span><span class="sxs-lookup"><span data-stu-id="61e3f-199">PRINTER\_ENUM\_NAME</span></span>                                | <span data-ttu-id="61e3f-200">« Fournisseur d’impression »</span><span class="sxs-lookup"><span data-stu-id="61e3f-200">"Print Provider"</span></span><br/>                 | <span data-ttu-id="61e3f-201">Tous les noms de domaine</span><span class="sxs-lookup"><span data-stu-id="61e3f-201">All domain names</span></span><br/>                                                                       |
| <span data-ttu-id="61e3f-202">nom de l’enum de l’imprimante \_ \_</span><span class="sxs-lookup"><span data-stu-id="61e3f-202">PRINTER\_ENUM\_NAME</span></span>                                | <span data-ttu-id="61e3f-203">«Fournisseur d’impression ! Domain</span><span class="sxs-lookup"><span data-stu-id="61e3f-203">"Print Provider!Domain"</span></span><br/>          | <span data-ttu-id="61e3f-204">Toutes les imprimantes et tous les serveurs d’impression dans le domaine de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="61e3f-204">All printers and print servers in the computer's domain</span></span><br/>                                |
| <span data-ttu-id="61e3f-205">nom de l’enum de l’imprimante \_ \_</span><span class="sxs-lookup"><span data-stu-id="61e3f-205">PRINTER\_ENUM\_NAME</span></span>                                | <span data-ttu-id="61e3f-206">«Fournisseur d’impression !! \\ \\ Usinage</span><span class="sxs-lookup"><span data-stu-id="61e3f-206">"Print Provider!!\\\\Machine"</span></span><br/>    | <span data-ttu-id="61e3f-207">Toutes les imprimantes partagées sur l' \\ \\ ordinateur</span><span class="sxs-lookup"><span data-stu-id="61e3f-207">All printers shared at \\\\Machine</span></span><br/>                                                     |
| <span data-ttu-id="61e3f-208">nom de l’enum de l’imprimante \_ \_</span><span class="sxs-lookup"><span data-stu-id="61e3f-208">PRINTER\_ENUM\_NAME</span></span>                                | <span data-ttu-id="61e3f-209">Une chaîne vide, ""</span><span class="sxs-lookup"><span data-stu-id="61e3f-209">An empty string, ""</span></span><br/>              | <span data-ttu-id="61e3f-210">Toutes les imprimantes locales.</span><span class="sxs-lookup"><span data-stu-id="61e3f-210">All local printers.</span></span><br/>                                                                    |
| <span data-ttu-id="61e3f-211">nom de l’enum de l’imprimante \_ \_</span><span class="sxs-lookup"><span data-stu-id="61e3f-211">PRINTER\_ENUM\_NAME</span></span>                                | <span data-ttu-id="61e3f-212">**NULL**</span><span class="sxs-lookup"><span data-stu-id="61e3f-212">**NULL**</span></span><br/>                         | <span data-ttu-id="61e3f-213">Tous les fournisseurs d’impression dans le domaine de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="61e3f-213">All print providers in the computer's domain</span></span><br/>                                           |
| <span data-ttu-id="61e3f-214">\_connexions d’énumération d’imprimantes \_</span><span class="sxs-lookup"><span data-stu-id="61e3f-214">PRINTER\_ENUM\_CONNECTIONS</span></span>                         | <span data-ttu-id="61e3f-215">Le paramètre *Name* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="61e3f-215">The *Name* parameter is ignored.</span></span><br/> | <span data-ttu-id="61e3f-216">Toutes les imprimantes distantes connectées</span><span class="sxs-lookup"><span data-stu-id="61e3f-216">All connected remote printers</span></span><br/>                                                          |
| <span data-ttu-id="61e3f-217">\_réseau d’énumération d’imprimantes \_</span><span class="sxs-lookup"><span data-stu-id="61e3f-217">PRINTER\_ENUM\_NETWORK</span></span>                             | <span data-ttu-id="61e3f-218">Le paramètre *Name* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="61e3f-218">The *Name* parameter is ignored.</span></span><br/> | <span data-ttu-id="61e3f-219">Toutes les imprimantes dans le domaine de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="61e3f-219">All printers in the computer's domain</span></span><br/>                                                  |
| <span data-ttu-id="61e3f-220">IMPRIMANTE \_ \_ à distance enum</span><span class="sxs-lookup"><span data-stu-id="61e3f-220">PRINTER\_ENUM\_REMOTE</span></span>                              | <span data-ttu-id="61e3f-221">Une chaîne vide, ""</span><span class="sxs-lookup"><span data-stu-id="61e3f-221">An empty string, ""</span></span><br/>              | <span data-ttu-id="61e3f-222">Toutes les imprimantes et tous les serveurs d’impression dans le domaine de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="61e3f-222">All printers and print servers in the computer's domain</span></span><br/>                                |
| <span data-ttu-id="61e3f-223">IMPRIMANTE \_ \_ à distance enum</span><span class="sxs-lookup"><span data-stu-id="61e3f-223">PRINTER\_ENUM\_REMOTE</span></span>                              | <span data-ttu-id="61e3f-224">« Fournisseur d’impression »</span><span class="sxs-lookup"><span data-stu-id="61e3f-224">"Print Provider"</span></span><br/>                 | <span data-ttu-id="61e3f-225">Identique au nom de l’enum de l’imprimante \_ \_</span><span class="sxs-lookup"><span data-stu-id="61e3f-225">Same as PRINTER\_ENUM\_NAME</span></span><br/>                                                            |
| <span data-ttu-id="61e3f-226">IMPRIMANTE \_ \_ à distance enum</span><span class="sxs-lookup"><span data-stu-id="61e3f-226">PRINTER\_ENUM\_REMOTE</span></span>                              | <span data-ttu-id="61e3f-227">«Fournisseur d’impression ! Domain</span><span class="sxs-lookup"><span data-stu-id="61e3f-227">"Print Provider!Domain"</span></span><br/>          | <span data-ttu-id="61e3f-228">Toutes les imprimantes et tous les serveurs d’impression dans le domaine de l’ordinateur, quel que soit le *domaine* spécifié.</span><span class="sxs-lookup"><span data-stu-id="61e3f-228">All printers and print servers in computer's domain, regardless of *Domain* specified.</span></span><br/> |
| <span data-ttu-id="61e3f-229">\_Catégorie d’énumération d’imprimantes \_ \_ 3D</span><span class="sxs-lookup"><span data-stu-id="61e3f-229">PRINTER\_ENUM\_CATEGORY\_3D</span></span>                        | <span data-ttu-id="61e3f-230">Le paramètre *Name* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="61e3f-230">The *Name* parameter is ignored.</span></span><br/> | <span data-ttu-id="61e3f-231">Seules les imprimantes 3D sont énumérées.</span><span class="sxs-lookup"><span data-stu-id="61e3f-231">Only 3D printers are enumerated.</span></span><br/>                                                       |
| <span data-ttu-id="61e3f-232">IMPRIMANTE \_ \_ catégorie \_ tout</span><span class="sxs-lookup"><span data-stu-id="61e3f-232">PRINTER\_ENUM\_CATEGORY\_ALL</span></span>                       | <span data-ttu-id="61e3f-233">Le paramètre *Name* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="61e3f-233">The *Name* parameter is ignored.</span></span><br/> | <span data-ttu-id="61e3f-234">les imprimantes 3D sont énumérées, ainsi que toutes les autres imprimantes.</span><span class="sxs-lookup"><span data-stu-id="61e3f-234">3D printers are enumerated, along with all other printers.</span></span><br/>                             |



 

## <a name="requirements"></a><span data-ttu-id="61e3f-235">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="61e3f-235">Requirements</span></span>



| <span data-ttu-id="61e3f-236">Condition requise</span><span class="sxs-lookup"><span data-stu-id="61e3f-236">Requirement</span></span> | <span data-ttu-id="61e3f-237">Valeur</span><span class="sxs-lookup"><span data-stu-id="61e3f-237">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61e3f-238">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="61e3f-238">Minimum supported client</span></span><br/> | <span data-ttu-id="61e3f-239">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="61e3f-239">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="61e3f-240">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="61e3f-240">Minimum supported server</span></span><br/> | <span data-ttu-id="61e3f-241">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="61e3f-241">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="61e3f-242">En-tête</span><span class="sxs-lookup"><span data-stu-id="61e3f-242">Header</span></span><br/>                   | <dl> <span data-ttu-id="61e3f-243"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="61e3f-243"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="61e3f-244">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="61e3f-244">Library</span></span><br/>                  | <dl> <span data-ttu-id="61e3f-245"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="61e3f-245"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="61e3f-246">DLL</span><span class="sxs-lookup"><span data-stu-id="61e3f-246">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61e3f-247"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="61e3f-247"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="61e3f-248">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="61e3f-248">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="61e3f-249">**EnumPrintersW** (Unicode) et **EnumPrintersA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="61e3f-249">**EnumPrintersW** (Unicode) and **EnumPrintersA** (ANSI)</span></span><br/>                                       |



## <a name="see-also"></a><span data-ttu-id="61e3f-250">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="61e3f-250">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61e3f-251">Impression</span><span class="sxs-lookup"><span data-stu-id="61e3f-251">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="61e3f-252">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="61e3f-252">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="61e3f-253">**AddPrinter**</span><span class="sxs-lookup"><span data-stu-id="61e3f-253">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="61e3f-254">**DeletePrinter**</span><span class="sxs-lookup"><span data-stu-id="61e3f-254">**DeletePrinter**</span></span>](deleteprinter.md)
</dt> <dt>

[<span data-ttu-id="61e3f-255">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="61e3f-255">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="61e3f-256">**\_Infos sur l’imprimante \_ 1**</span><span class="sxs-lookup"><span data-stu-id="61e3f-256">**PRINTER\_INFO\_1**</span></span>](printer-info-1.md)
</dt> <dt>

[<span data-ttu-id="61e3f-257">**\_Infos sur l’imprimante \_ 2**</span><span class="sxs-lookup"><span data-stu-id="61e3f-257">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="61e3f-258">**\_Infos sur l’imprimante \_ 4**</span><span class="sxs-lookup"><span data-stu-id="61e3f-258">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> <dt>

[<span data-ttu-id="61e3f-259">**\_Infos sur l’imprimante \_ 5**</span><span class="sxs-lookup"><span data-stu-id="61e3f-259">**PRINTER\_INFO\_5**</span></span>](printer-info-5.md)
</dt> <dt>

[<span data-ttu-id="61e3f-260">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="61e3f-260">**SetPrinter**</span></span>](setprinter.md)
</dt> </dl>

 

