---
description: Génère un nombre aléatoire sécurisé à l’aide du fournisseur de services de chiffrement (CSP) par défaut.
ms.assetid: 52c49f73-58b8-455f-9368-54f38de55776
title: Méthode Utilities. GetRandom
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.GetRandom
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3b7e02c7df61c1a2d710189fb2e5e0a21cc0b504
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540272"
---
# <a name="utilitiesgetrandom-method"></a><span data-ttu-id="69e7c-103">Méthode Utilities. GetRandom</span><span class="sxs-lookup"><span data-stu-id="69e7c-103">Utilities.GetRandom method</span></span>

<span data-ttu-id="69e7c-104">\[La méthode **GetRandom** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.\]</span><span class="sxs-lookup"><span data-stu-id="69e7c-104">\[The **GetRandom** method is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="69e7c-105">La méthode **GetRandom** génère un nombre aléatoire sécurisé à l’aide du [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP) par défaut.</span><span class="sxs-lookup"><span data-stu-id="69e7c-105">The **GetRandom** method generates a secure random number using the default [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

## <a name="syntax"></a><span data-ttu-id="69e7c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="69e7c-106">Syntax</span></span>


```VB
Utilities.GetRandom( _
  [ ByVal Length ], _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="69e7c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="69e7c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69e7c-108">*Longueur* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="69e7c-108">*Length* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="69e7c-109">Longueur, en octets, du nombre aléatoire à créer.</span><span class="sxs-lookup"><span data-stu-id="69e7c-109">The length, in bytes, of the random number to create.</span></span> <span data-ttu-id="69e7c-110">La valeur par défaut est de 8 octets.</span><span class="sxs-lookup"><span data-stu-id="69e7c-110">The default value is 8 bytes.</span></span>

</dd> <dt>

<span data-ttu-id="69e7c-111">*EncodingType* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="69e7c-111">*EncodingType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="69e7c-112">Valeur de l’énumération de [**\_ \_ type d’encodage**](capicom-encoding-type.md) CAPICOM qui indique le type d’encodage à utiliser pour le nombre aléatoire généré.</span><span class="sxs-lookup"><span data-stu-id="69e7c-112">A value of the [**CAPICOM\_ENCODING\_TYPE**](capicom-encoding-type.md) enumeration that indicates the type of encoding to use for the generated random number.</span></span> <span data-ttu-id="69e7c-113">La valeur par défaut est l' \_ encodage d’un \_ binaire CAPICOM.</span><span class="sxs-lookup"><span data-stu-id="69e7c-113">The default value is CAPICOM\_ENCODE\_BINARY.</span></span> <span data-ttu-id="69e7c-114">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="69e7c-114">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="69e7c-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="69e7c-115">Value</span></span>                                                                                                                                                                                  | <span data-ttu-id="69e7c-116">Signification</span><span class="sxs-lookup"><span data-stu-id="69e7c-116">Meaning</span></span>                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <span data-ttu-id="69e7c-117"><dt>**\_coder \_ tout**</dt></span><span class="sxs-lookup"><span data-stu-id="69e7c-117"><dt>**CAPICOM\_ENCODE\_ANY**</dt></span></span> </dl>          | <span data-ttu-id="69e7c-118">Ce type d’encodage est utilisé uniquement lorsque les données d’entrée ont un type d’encodage inconnu.</span><span class="sxs-lookup"><span data-stu-id="69e7c-118">This encoding type is used only when the input data has an unknown encoding type.</span></span> <span data-ttu-id="69e7c-119">Si cette valeur est utilisée pour spécifier le type d’encodage de la sortie, CAPICOM est utilisé à la \_ \_ place.</span><span class="sxs-lookup"><span data-stu-id="69e7c-119">If this value is used to specify the output's encoding type, CAPICOM\_ENCODE\_BASE64 will be used instead.</span></span> <span data-ttu-id="69e7c-120">Introduit dans CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="69e7c-120">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <span data-ttu-id="69e7c-121"><dt>**\_Encode \_ Base64**</dt></span><span class="sxs-lookup"><span data-stu-id="69e7c-121"><dt>**CAPICOM\_ENCODE\_BASE64**</dt></span></span> </dl> | <span data-ttu-id="69e7c-122">Les données sont enregistrées sous la forme d’une chaîne encodée en base64.</span><span class="sxs-lookup"><span data-stu-id="69e7c-122">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <span data-ttu-id="69e7c-123"><dt>**codage d’un \_ \_ fichier binaire CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="69e7c-123"><dt>**CAPICOM\_ENCODE\_BINARY**</dt></span></span> </dl> | <span data-ttu-id="69e7c-124">Les données sont enregistrées sous la forme d’une séquence binaire pure.</span><span class="sxs-lookup"><span data-stu-id="69e7c-124">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69e7c-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="69e7c-125">Return value</span></span>

<span data-ttu-id="69e7c-126">Nombre d’octets de *longueur* numérique généré de manière aléatoire, avec l’encodage spécifié.</span><span class="sxs-lookup"><span data-stu-id="69e7c-126">A randomly generated number *Length* bytes long, with the specified encoding.</span></span>

## <a name="requirements"></a><span data-ttu-id="69e7c-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="69e7c-127">Requirements</span></span>



| <span data-ttu-id="69e7c-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="69e7c-128">Requirement</span></span> | <span data-ttu-id="69e7c-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="69e7c-129">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="69e7c-130">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="69e7c-130">Redistributable</span></span><br/> | <span data-ttu-id="69e7c-131">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="69e7c-131">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="69e7c-132">DLL</span><span class="sxs-lookup"><span data-stu-id="69e7c-132">DLL</span></span><br/>             | <dl> <span data-ttu-id="69e7c-133"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69e7c-133"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69e7c-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69e7c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69e7c-135">**Services**</span><span class="sxs-lookup"><span data-stu-id="69e7c-135">**Utilities**</span></span>](utilities.md)
</dt> </dl>

 

 
