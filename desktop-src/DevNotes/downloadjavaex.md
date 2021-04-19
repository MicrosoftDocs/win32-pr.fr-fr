---
description: Télécharge la signature du fichier. cab, vérifie les autorisations associées aux packages et les exécute en fonction de l’authentification.
ms.assetid: b86a8f39-73a1-4e17-ac83-9ed095de4922
title: DownloadJavaEX fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownloadJavaEX
api_type:
- DllExport
api_location:
- Javacypt.dll
ms.openlocfilehash: 31371e91599d604db591ee3e921b42bc809aae21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541134"
---
# <a name="downloadjavaex-function"></a><span data-ttu-id="115a5-103">DownloadJavaEX fonction)</span><span class="sxs-lookup"><span data-stu-id="115a5-103">DownloadJavaEX function</span></span>

<span data-ttu-id="115a5-104">Télécharge la signature du fichier. cab, vérifie les autorisations associées aux packages et les exécute en fonction de l’authentification.</span><span class="sxs-lookup"><span data-stu-id="115a5-104">Downloads the .cab file signature, verifies the permissions associated with the packages, and executes them based on authentication.</span></span>

## <a name="syntax"></a><span data-ttu-id="115a5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="115a5-105">Syntax</span></span>


```C++
HRESULT WINAPI DownloadJavaEX(
  _In_ PALLOCATOR               Reserved,
  _In_ PCRYPT_PROVIDER_DATA     pProviderData,
  _In_ PJAVA_POLICY_PROVIDER    pJava,
  _In_ CRYPT_PROVIDER_FUNCTIONS *pFunctions,
  _In_ BOOL                     fCertificate,
  _In_ PJAVA_TRUST              pTrust
);
```



## <a name="parameters"></a><span data-ttu-id="115a5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="115a5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="115a5-107">*Réservé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="115a5-107">*Reserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="115a5-108">Ce paramètre est réservé.</span><span class="sxs-lookup"><span data-stu-id="115a5-108">This parameter is reserved.</span></span>

</dd> <dt>

<span data-ttu-id="115a5-109">*pProviderData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="115a5-109">*pProviderData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="115a5-110">Structure [**de \_ \_ données de fournisseur**](/windows/win32/api/wintrust/ns-wintrust-crypt_provider_data) de chiffre qui contient des données de certificat telles que des autorisations de fichier et de zone.</span><span class="sxs-lookup"><span data-stu-id="115a5-110">A [**CRYPT\_PROVIDER\_DATA**](/windows/win32/api/wintrust/ns-wintrust-crypt_provider_data) structure that contains certificate data such as file and zone permissions.</span></span>

</dd> <dt>

<span data-ttu-id="115a5-111">*pJava* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="115a5-111">*pJava* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="115a5-112">Structure [**de \_ \_ fournisseur de stratégies Java**](/previous-versions//bb432350(v=vs.85)) qui contient les données relatives au fournisseur de stratégie.</span><span class="sxs-lookup"><span data-stu-id="115a5-112">A [**JAVA\_POLICY\_PROVIDER**](/previous-versions//bb432350(v=vs.85)) structure that contains data related to the policy provider.</span></span>

</dd> <dt>

<span data-ttu-id="115a5-113">*pFunctions* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="115a5-113">*pFunctions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="115a5-114">Structure [**de \_ \_ fonctions du fournisseur**](/windows/win32/api/wintrust/ns-wintrust-crypt_provider_functions) de chiffrement qui contient une liste de méthodes pour vérifier des objets de certificat, des signatures et des stratégies finales.</span><span class="sxs-lookup"><span data-stu-id="115a5-114">A [**CRYPT\_PROVIDER\_FUNCTIONS**](/windows/win32/api/wintrust/ns-wintrust-crypt_provider_functions) structure that contains a list of methods to verify certificate objects, signatures, and final policies.</span></span>

</dd> <dt>

<span data-ttu-id="115a5-115">*fCertificate* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="115a5-115">*fCertificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="115a5-116">Si un certificat est présent, ce paramètre a la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="115a5-116">If a certificate is present, this parameter is **TRUE**.</span></span> <span data-ttu-id="115a5-117">Sinon, la **valeur est false**.</span><span class="sxs-lookup"><span data-stu-id="115a5-117">Otherwise, it is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="115a5-118">*pTrust* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="115a5-118">*pTrust* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="115a5-119">Structure [**d' \_ approbation Java**](/windows/desktop/api/Capi/ns-capi-java_trust) qui contient des informations d’approbation, telles que l’autorisation encodée, la signature de l’encodeur et le code de stratégie de retour authentique.</span><span class="sxs-lookup"><span data-stu-id="115a5-119">A [**JAVA\_TRUST**](/windows/desktop/api/Capi/ns-capi-java_trust) structure that contains trust information such as encoded permission, encoder signature, and authentic return policy code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="115a5-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="115a5-120">Return value</span></span>

<span data-ttu-id="115a5-121">Si la fonction est réussie, la valeur de retour est **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="115a5-121">If the function succeeds, the return value is **S\_OK**.</span></span> <span data-ttu-id="115a5-122">Dans le cas contraire, la valeur de retour est un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="115a5-122">Otherwise, the return value is an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="115a5-123">Notes</span><span class="sxs-lookup"><span data-stu-id="115a5-123">Remarks</span></span>

<span data-ttu-id="115a5-124">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="115a5-124">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="115a5-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="115a5-125">Requirements</span></span>



| <span data-ttu-id="115a5-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="115a5-126">Requirement</span></span> | <span data-ttu-id="115a5-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="115a5-127">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="115a5-128">DLL</span><span class="sxs-lookup"><span data-stu-id="115a5-128">DLL</span></span><br/> | <dl> <span data-ttu-id="115a5-129"><dt>Javacypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="115a5-129"><dt>Javacypt.dll</dt></span></span> </dl> |



 

 
