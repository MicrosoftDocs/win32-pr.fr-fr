---
description: Exporte le matériel de génération de clé selon la norme RFC 5705.
ms.assetid: 19624852-B1A6-4BB4-96AF-0457834DA294
title: SslExportKeyingMaterial, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslExportKeyingMaterial
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 906a7535b297f309c0c8471843ce07f43a110a3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760107"
---
# <a name="sslexportkeyingmaterial-function"></a><span data-ttu-id="c1329-103">SslExportKeyingMaterial fonction)</span><span class="sxs-lookup"><span data-stu-id="c1329-103">SslExportKeyingMaterial function</span></span>

<span data-ttu-id="c1329-104">Exporte le matériel de génération de clé selon la [norme RFC 5705](https://tools.ietf.org/html/rfc5705).</span><span class="sxs-lookup"><span data-stu-id="c1329-104">Exports keying material per the [RFC 5705 standard](https://tools.ietf.org/html/rfc5705).</span></span> <span data-ttu-id="c1329-105">Cette fonction utilise la fonction TLS aléatoire pour produire une mémoire tampon d’octets de l’élément de clé.</span><span class="sxs-lookup"><span data-stu-id="c1329-105">This function uses the TLS pseudorandom function to produce a byte buffer of keying material.</span></span> <span data-ttu-id="c1329-106">Elle prend une référence au secret principal, l’étiquette disambiguating ASCII, les valeurs aléatoires client et serveur, et éventuellement les données de contexte de l’application.</span><span class="sxs-lookup"><span data-stu-id="c1329-106">It takes a reference to the master secret, the disambiguating ASCII label, client and server random values, and optionally the application context data.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1329-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c1329-107">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslExportKeyingMaterial(
  _In_     NCRYPT_PROV_HANDLE hSslProvider,
  _In_     NCRYPT_KEY_HANDLE  hMasterKey,
  _In_     PCHAR              sLabel,
  _In_     PBYTE              pbRandoms,
  _In_     DWORD              cbRandoms,
  _In_opt_ PBYTE              pbContextValue,
  _In_     WORD               cbContextValue,
  _Out_    PBYTE              pbOutput,
  _In_     DWORD              cbOutput,
  _In_     DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="c1329-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c1329-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1329-109">*hSslProvider* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c1329-109">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1329-110">Handle de l’instance du fournisseur de protocole TLS.</span><span class="sxs-lookup"><span data-stu-id="c1329-110">The handle of the TLS protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="c1329-111">*hMasterKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c1329-111">*hMasterKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1329-112">Handle de l’objet de clé principale qui sera utilisé pour créer le support de génération de clés à br exporté.</span><span class="sxs-lookup"><span data-stu-id="c1329-112">The handle of the master key object that will be used to create the keying material to br exported.</span></span>

</dd> <dt>

<span data-ttu-id="c1329-113">*slabel* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c1329-113">*sLabel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1329-114">chaîne d’étiquette ASCII terminée par un caractère NUL.</span><span class="sxs-lookup"><span data-stu-id="c1329-114">a NUL-terminated ASCII label string.</span></span> <span data-ttu-id="c1329-115">Schannel supprime le caractère null de fin avant de le passer à la fonction Pseudo-aléatoire.</span><span class="sxs-lookup"><span data-stu-id="c1329-115">Schannel will remove the terminating NUL character before passing it to the pseudorandom function.</span></span>

</dd> <dt>

<span data-ttu-id="c1329-116">*pbRandoms* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c1329-116">*pbRandoms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1329-117">Pointeur vers une mémoire tampon qui contient une concaténation des valeurs aléatoires *\_ aléatoires du client* et du *serveur \_* de la connexion TLS.</span><span class="sxs-lookup"><span data-stu-id="c1329-117">A pointer to a buffer that contains a concatenation of the *client\_random* and *server\_random* values of the TLS connection.</span></span>

</dd> <dt>

<span data-ttu-id="c1329-118">*cbRandoms* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c1329-118">*cbRandoms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1329-119">Longueur, en octets, de la mémoire tampon *pbRandoms* .</span><span class="sxs-lookup"><span data-stu-id="c1329-119">The length, in bytes, of the *pbRandoms* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="c1329-120">*pbContextValue* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="c1329-120">*pbContextValue* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c1329-121">Pointeur vers une mémoire tampon qui contient le contexte d’application.</span><span class="sxs-lookup"><span data-stu-id="c1329-121">A pointer to a buffer that contains the application context.</span></span> <span data-ttu-id="c1329-122">Si *pbContextValue* a la **valeur null**, *cbContextValue* doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="c1329-122">If *pbContextValue* is **NULL**, *cbContextValue* must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c1329-123">*cbContextValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c1329-123">*cbContextValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1329-124">Longueur, en octets, de la mémoire tampon *pbContextValue* .</span><span class="sxs-lookup"><span data-stu-id="c1329-124">The length, in bytes, of the *pbContextValue* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="c1329-125">*pbOutput* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c1329-125">*pbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c1329-126">Adresse d’une mémoire tampon qui reçoit le support de génération de clé exporté.</span><span class="sxs-lookup"><span data-stu-id="c1329-126">The address of a buffer that receives the exported keying material.</span></span> <span data-ttu-id="c1329-127">Le paramètre *cbOutput* contient la taille de cette mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="c1329-127">The *cbOutput* parameter contains the size of this buffer.</span></span> <span data-ttu-id="c1329-128">Cette valeur ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="c1329-128">This value cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c1329-129">*cbOutput* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c1329-129">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1329-130">Longueur, en octets, de la mémoire tampon *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="c1329-130">The length, in bytes, of the *pbOutput* buffer.</span></span> <span data-ttu-id="c1329-131">Doit être supérieur à zéro.</span><span class="sxs-lookup"><span data-stu-id="c1329-131">Must be greater than zero.</span></span>

</dd> <dt>

<span data-ttu-id="c1329-132">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c1329-132">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1329-133">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="c1329-133">Not used.</span></span> <span data-ttu-id="c1329-134">Doit être défini à zéro.</span><span class="sxs-lookup"><span data-stu-id="c1329-134">Must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1329-135">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c1329-135">Return value</span></span>

<span data-ttu-id="c1329-136">Si la fonction est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="c1329-136">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="c1329-137">Si la fonction échoue, elle retourne une valeur d’erreur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="c1329-137">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="c1329-138">Les codes de retour possibles incluent, mais ne sont pas limités à, les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="c1329-138">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="c1329-139">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="c1329-139">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="c1329-140">Description</span><span class="sxs-lookup"><span data-stu-id="c1329-140">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="c1329-141"><dt>**NPD \_ \_Handle 0X80090026L non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="c1329-141"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="c1329-142">L’un des handles fournis n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="c1329-142">One of the provided handles is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c1329-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c1329-143">Requirements</span></span>



| <span data-ttu-id="c1329-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c1329-144">Requirement</span></span> | <span data-ttu-id="c1329-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1329-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1329-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c1329-146">Minimum supported client</span></span><br/> | <span data-ttu-id="c1329-147">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c1329-147">Windows 10 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="c1329-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c1329-148">Minimum supported server</span></span><br/> | <span data-ttu-id="c1329-149">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c1329-149">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c1329-150">En-tête</span><span class="sxs-lookup"><span data-stu-id="c1329-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1329-151"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1329-151"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="c1329-152">DLL</span><span class="sxs-lookup"><span data-stu-id="c1329-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1329-153"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1329-153"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

 




