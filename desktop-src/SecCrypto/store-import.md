---
description: La méthode d’importation copie dans un magasin de certificats ouvert le contenu d’un magasin de certificats précédemment exporté. Cette méthode peut uniquement être utilisée avec un magasin qui a été ouvert avec l’autorisation de lecture/écriture.
ms.assetid: 22db8f1c-469b-4baf-9039-4da35c9c6aa0
title: Store. Import, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Import
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4eb16cc341eb6e5dcee87216a52e9e3de94d1b65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528820"
---
# <a name="storeimport-method"></a><span data-ttu-id="22c92-104">Store. Import, méthode</span><span class="sxs-lookup"><span data-stu-id="22c92-104">Store.Import method</span></span>

<span data-ttu-id="22c92-105">\[La méthode d' **importation** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="22c92-105">\[The **Import** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="22c92-106">Utilisez plutôt la [**classe X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="22c92-106">Instead, use the [**X509Store Class**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="22c92-107">La méthode d' **importation** copie dans un [*magasin de certificats*](../secgloss/c-gly.md) ouvert le contenu d’un magasin de certificats précédemment exporté.</span><span class="sxs-lookup"><span data-stu-id="22c92-107">The **Import** method copies into an open [*certificate store*](../secgloss/c-gly.md) the contents of a previously exported certificate store.</span></span> <span data-ttu-id="22c92-108">Cette méthode peut uniquement être utilisée avec un magasin qui a été ouvert avec l’autorisation de lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="22c92-108">This method can only be used with a store that has been opened with read/write permission.</span></span>

## <a name="syntax"></a><span data-ttu-id="22c92-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="22c92-109">Syntax</span></span>


```VB
Store.Import( _
  ByVal EncodedStore _
)
```



## <a name="parameters"></a><span data-ttu-id="22c92-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="22c92-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22c92-111">*EncodedStore* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="22c92-111">*EncodedStore* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22c92-112">Chaîne qui contient les certificats encodés à importer.</span><span class="sxs-lookup"><span data-stu-id="22c92-112">The string that contains the encoded certificates to be imported.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22c92-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="22c92-113">Return value</span></span>

<span data-ttu-id="22c92-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="22c92-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="22c92-115">Notes</span><span class="sxs-lookup"><span data-stu-id="22c92-115">Remarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="22c92-116">Lorsque cette méthode est appelée à partir d’un script Web, le script doit accéder aux certificats numériques sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="22c92-116">When this method is called from a web script, the script needs to access digital certificates on the local computer.</span></span> <span data-ttu-id="22c92-117">Si vous autorisez le script à accéder à vos certificats numériques, le site Web à partir duquel le script est exécuté aura également accès aux informations personnelles stockées dans les certificats.</span><span class="sxs-lookup"><span data-stu-id="22c92-117">If you allow the script to access your digital certificates, the website from which the script is run will also gain access to any personal information stored in the certificates.</span></span> <span data-ttu-id="22c92-118">La première fois que cette méthode est appelée à partir d’un domaine particulier, une boîte de dialogue est générée dans laquelle l’utilisateur doit indiquer si l’accès aux certificats doit être autorisé.</span><span class="sxs-lookup"><span data-stu-id="22c92-118">The first time this method is called from a particular domain, a dialog box is generated in which the user must indicate whether access to the certificates should be allowed.</span></span>

 

<span data-ttu-id="22c92-119">Si le magasin n’est pas ouvert avec l’autorisation de lecture/écriture, cette méthode échoue.</span><span class="sxs-lookup"><span data-stu-id="22c92-119">If the store is not opened with read/write permission, this method fails.</span></span> <span data-ttu-id="22c92-120">Bien que cette méthode puisse être utilisée avec les magasins de mémoire, toute modification apportée à un magasin de mémoire n’est pas conservée lors de la fermeture de la Banque.</span><span class="sxs-lookup"><span data-stu-id="22c92-120">Although this method can be used with memory stores, any changes made to a memory store are not persisted when the store is closed.</span></span>

## <a name="requirements"></a><span data-ttu-id="22c92-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="22c92-121">Requirements</span></span>



| <span data-ttu-id="22c92-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="22c92-122">Requirement</span></span> | <span data-ttu-id="22c92-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="22c92-123">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="22c92-124">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="22c92-124">Redistributable</span></span><br/> | <span data-ttu-id="22c92-125">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="22c92-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="22c92-126">DLL</span><span class="sxs-lookup"><span data-stu-id="22c92-126">DLL</span></span><br/>             | <dl> <span data-ttu-id="22c92-127"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22c92-127"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22c92-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="22c92-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22c92-129">**Magasin**</span><span class="sxs-lookup"><span data-stu-id="22c92-129">**Store**</span></span>](store.md)
</dt> <dt>

[<span data-ttu-id="22c92-130">**Objets de chiffrement**</span><span class="sxs-lookup"><span data-stu-id="22c92-130">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
