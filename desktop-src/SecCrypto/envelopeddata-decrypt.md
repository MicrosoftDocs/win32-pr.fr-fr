---
description: Déchiffre le contenu enveloppé.
ms.assetid: 717d0595-e8bb-4725-bd53-fc1281cbc8ee
title: EnvelopedData. Decrypt, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData.Decrypt
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0c4c71ba0e3e0c2d421ad7bcbc9b1a61bb71d284
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541104"
---
# <a name="envelopeddatadecrypt-method"></a><span data-ttu-id="29197-103">EnvelopedData. Decrypt, méthode</span><span class="sxs-lookup"><span data-stu-id="29197-103">EnvelopedData.Decrypt method</span></span>

<span data-ttu-id="29197-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="29197-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="29197-105">Utilisez plutôt la [**classe EnvelopedCms**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="29197-105">Instead, use the [**EnvelopedCms Class**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="29197-106">La méthode **Decrypt** déchiffre le contenu enveloppé.</span><span class="sxs-lookup"><span data-stu-id="29197-106">The **Decrypt** method decrypts enveloped content.</span></span> <span data-ttu-id="29197-107">Le déchiffrement s’effectue si le destinataire du message a accès à la [*clé privée*](../secgloss/p-gly.md) associée à l’une des [*clés publiques*](../secgloss/p-gly.md) utilisées pour encapsuler le message.</span><span class="sxs-lookup"><span data-stu-id="29197-107">Decryption is done if the recipient of the message has access to the [*private key*](../secgloss/p-gly.md) paired with one of the [*public keys*](../secgloss/p-gly.md) used to envelop the message.</span></span> <span data-ttu-id="29197-108">L’appel de la méthode **Decrypt** réinitialise l' [*État*](../secgloss/s-gly.md) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="29197-108">Calling the **Decrypt** method resets the [*state*](../secgloss/s-gly.md) of the object.</span></span> <span data-ttu-id="29197-109">Si la méthode de **déchiffrement** est établie, la propriété [**contenu**](envelopeddata-content.md) de l’objet [**EnvelopedData**](envelopeddata.md) est définie sur le message de texte en clair.</span><span class="sxs-lookup"><span data-stu-id="29197-109">If the **Decrypt** method succeeds, the [**Content**](envelopeddata-content.md) property of the [**EnvelopedData**](envelopeddata.md) object is set to the plaintext message.</span></span>

## <a name="syntax"></a><span data-ttu-id="29197-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="29197-110">Syntax</span></span>


```VB
EnvelopedData.Decrypt( _
  ByVal EnvelopedMessage _
)
```



## <a name="parameters"></a><span data-ttu-id="29197-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="29197-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29197-112">*EnvelopedMessage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="29197-112">*EnvelopedMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29197-113">Chaîne qui contient les données enveloppées à déchiffrer.</span><span class="sxs-lookup"><span data-stu-id="29197-113">String that contains the enveloped data to be decrypted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29197-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="29197-114">Return value</span></span>

<span data-ttu-id="29197-115">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="29197-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="29197-116">Notes</span><span class="sxs-lookup"><span data-stu-id="29197-116">Remarks</span></span>

<span data-ttu-id="29197-117">Les données déchiffrées deviennent la valeur de la propriété de [**contenu**](envelopeddata-content.md) de l’objet [**EnvelopedData**](envelopeddata.md) .</span><span class="sxs-lookup"><span data-stu-id="29197-117">The decrypted data becomes the [**Content**](envelopeddata-content.md) property value for the [**EnvelopedData**](envelopeddata.md) object.</span></span>

<span data-ttu-id="29197-118">Si l’utilisateur de cette méthode n’a pas accès à une clé privée qui correspond à l’une des clés publiques utilisées pour encapsuler le message, la méthode échoue.</span><span class="sxs-lookup"><span data-stu-id="29197-118">If the user of this method does not have access to a private key that matches one of the public keys used to envelop the message, the method fails.</span></span> <span data-ttu-id="29197-119">Cette méthode échoue si le certificat de la clé privée associée ne figure pas dans l’ordinateur local mon magasin ou dans le magasin de l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="29197-119">This method will fail if the certificate for the associated private key is not in either the local computer MY store or the current user MY store.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="29197-120">Lorsque cette méthode est appelée à partir d’un script Web, le script doit utiliser votre [*clé privée*](../secgloss/p-gly.md) pour déchiffrer les données.</span><span class="sxs-lookup"><span data-stu-id="29197-120">When this method is called from a web script, the script needs to use your [*private key*](../secgloss/p-gly.md) to decrypt the data.</span></span> <span data-ttu-id="29197-121">Autoriser les sites Web non approuvés à utiliser votre clé privée est un risque pour la sécurité.</span><span class="sxs-lookup"><span data-stu-id="29197-121">Allowing untrusted websites to use your private key is a security risk.</span></span> <span data-ttu-id="29197-122">Une boîte de dialogue qui vous demande si le site Web peut utiliser votre clé privée s’affiche lorsque cette méthode est appelée pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="29197-122">A dialog box that asks whether the website can use your private key appears when this method is first called.</span></span> <span data-ttu-id="29197-123">Si vous autorisez le script à utiliser votre clé privée et que vous sélectionnez ne plus me le demander, la boîte de dialogue n’apparaît plus pour les scripts qui utilisent votre clé privée pour déchiffrer les données dans ce domaine.</span><span class="sxs-lookup"><span data-stu-id="29197-123">If you allow the script to use your private key and select "Do not ask me this again," the dialog box will no longer appear for any script that uses your private key to decrypt data within that domain.</span></span> <span data-ttu-id="29197-124">Toutefois, les scripts en dehors de ce domaine qui tentent d’utiliser votre clé privée pour déchiffrer des données entraînent l’affichage de cette boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="29197-124">However, scripts outside that domain that attempt to use your private key to decrypt data will still cause this dialog box to appear.</span></span> <span data-ttu-id="29197-125">Si vous n’autorisez pas le script à utiliser votre clé privée et que vous sélectionnez ne plus me le demander, les scripts de ce domaine se verront automatiquement refuser la possibilité d’utiliser votre clé privée pour déchiffrer les données.</span><span class="sxs-lookup"><span data-stu-id="29197-125">If you do not allow the script to use your private key and select "Do not ask me this again," scripts within that domain will automatically be refused the ability to use your private key to decrypt data.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="29197-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="29197-126">Requirements</span></span>



| <span data-ttu-id="29197-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="29197-127">Requirement</span></span> | <span data-ttu-id="29197-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="29197-128">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="29197-129">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="29197-129">End of client support</span></span><br/> | <span data-ttu-id="29197-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="29197-130">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="29197-131">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="29197-131">End of server support</span></span><br/> | <span data-ttu-id="29197-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="29197-132">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="29197-133">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="29197-133">Redistributable</span></span><br/>       | <span data-ttu-id="29197-134">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="29197-134">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="29197-135">DLL</span><span class="sxs-lookup"><span data-stu-id="29197-135">DLL</span></span><br/>                   | <dl> <span data-ttu-id="29197-136"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29197-136"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29197-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29197-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29197-138">**Objets de chiffrement**</span><span class="sxs-lookup"><span data-stu-id="29197-138">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="29197-139">**EnvelopedData**</span><span class="sxs-lookup"><span data-stu-id="29197-139">**EnvelopedData**</span></span>](envelopeddata.md)
</dt> </dl>

 

 
