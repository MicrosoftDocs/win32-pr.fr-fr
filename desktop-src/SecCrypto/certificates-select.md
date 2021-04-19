---
description: Affiche une boîte de dialogue permettant de sélectionner des certificats et retourne une collection de ces certificats sélectionnés.
ms.assetid: dbf49a4b-6da1-4819-afcd-46db89a00fce
title: 'ICertificates2 :: Select, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Select
- ICertificates2.Select
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: cfd5b1cb5e269c14e05de25262fda711549bf02d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534896"
---
# <a name="icertificates2select-method"></a><span data-ttu-id="b8240-103">ICertificates2 :: Select, méthode</span><span class="sxs-lookup"><span data-stu-id="b8240-103">ICertificates2::Select method</span></span>

<span data-ttu-id="b8240-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b8240-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="b8240-105">Utilisez plutôt la [**classe X509Certificate2Collection**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="b8240-105">Instead, use the [**X509Certificate2Collection Class**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="b8240-106">La méthode **Select** affiche une boîte de dialogue permettant de sélectionner des certificats et renvoie une collection des certificats sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="b8240-106">The **Select** method displays a dialog box for selecting certificates and returns a collection of those certificates selected.</span></span> <span data-ttu-id="b8240-107">Cette méthode a été introduite dans CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="b8240-107">This method was introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8240-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b8240-108">Syntax</span></span>


```VB
Certificates.Select( _
  [ ByVal Title ], _
  [ ByVal DisplayString ], _
  [ ByVal bMultiSelect ] _
)
```



## <a name="parameters"></a><span data-ttu-id="b8240-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b8240-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8240-110">*Titre* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="b8240-110">*Title* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b8240-111">Chaîne qui contient le titre de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="b8240-111">String that contains the title for the dialog box.</span></span> <span data-ttu-id="b8240-112">La valeur par défaut est une chaîne vide ("").</span><span class="sxs-lookup"><span data-stu-id="b8240-112">The default value is an empty string ("").</span></span>

</dd> <dt>

<span data-ttu-id="b8240-113">*DisplayString* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="b8240-113">*DisplayString* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b8240-114">Chaîne qui contient le texte d’invite affiché avec la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="b8240-114">String that contains the prompt text displayed with the dialog box.</span></span> <span data-ttu-id="b8240-115">La valeur par défaut est une chaîne vide ("").</span><span class="sxs-lookup"><span data-stu-id="b8240-115">The default value is an empty string ("").</span></span>

</dd> <dt>

<span data-ttu-id="b8240-116">*bMultiSelect* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="b8240-116">*bMultiSelect* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b8240-117">Valeur booléenne qui indique si l’utilisateur peut sélectionner plusieurs certificats.</span><span class="sxs-lookup"><span data-stu-id="b8240-117">Boolean value that indicates whether the user can select more than one certificate.</span></span> <span data-ttu-id="b8240-118">True indique qu’il est possible de sélectionner plusieurs certificats à l’aide de la touche CTRL ou Maj.</span><span class="sxs-lookup"><span data-stu-id="b8240-118">True indicates multiple certificates can be selected by using the CTRL or SHIFT key.</span></span> <span data-ttu-id="b8240-119">La valeur par défaut est false.</span><span class="sxs-lookup"><span data-stu-id="b8240-119">The default value is false.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8240-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b8240-120">Return value</span></span>

<span data-ttu-id="b8240-121">Objet de [**certificats**](certificates.md) qui contient les certificats sélectionnés dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="b8240-121">A [**Certificates**](certificates.md) object that contains the certificates selected from the dialog box.</span></span>

<span data-ttu-id="b8240-122">**Capicom 2,1 :** L’objet de [**certificats**](certificates.md) retourné contient des références aux certificats de la collection à partir de laquelle la sélection a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="b8240-122">**CAPICOM 2.1:** The [**Certificates**](certificates.md) object that is returned contains references to the certificates in the collection from which the selection was made.</span></span> <span data-ttu-id="b8240-123">Toutes les modifications apportées aux certificats de l’objet **certificats** retournés sont répercutées dans cette collection.</span><span class="sxs-lookup"><span data-stu-id="b8240-123">Any changes made to the certificates in the returned **Certificates** object are reflected in that collection.</span></span>

<span data-ttu-id="b8240-124">**Capicom 2,0, CAPICOM 2.0.0.1, CAPICOM 2.0.0.2 et ca-2.0.0.3** de la façon suivante : L’objet de [**certificats**](certificates.md) retourné contient des copies des certificats dans la collection à partir de laquelle la sélection a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="b8240-124">**CAPICOM 2.0, CAPICOM 2.0.0.1, CAPICOM 2.0.0.2, and CAPICOM 2.0.0.3:** The [**Certificates**](certificates.md) object that is returned contains copies of the certificates in the collection from which the selection was made.</span></span> <span data-ttu-id="b8240-125">Les modifications apportées aux certificats de l’objet **certificats** retournés ne sont pas reflétées dans cette collection.</span><span class="sxs-lookup"><span data-stu-id="b8240-125">Any changes made to the certificates in the returned **Certificates** object are not reflected in that collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8240-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b8240-126">Requirements</span></span>



| <span data-ttu-id="b8240-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b8240-127">Requirement</span></span> | <span data-ttu-id="b8240-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8240-128">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8240-129">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="b8240-129">End of client support</span></span><br/> | <span data-ttu-id="b8240-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b8240-130">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="b8240-131">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="b8240-131">End of server support</span></span><br/> | <span data-ttu-id="b8240-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b8240-132">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="b8240-133">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="b8240-133">Redistributable</span></span><br/>       | <span data-ttu-id="b8240-134">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="b8240-134">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="b8240-135">DLL</span><span class="sxs-lookup"><span data-stu-id="b8240-135">DLL</span></span><br/>                   | <dl> <span data-ttu-id="b8240-136"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8240-136"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
