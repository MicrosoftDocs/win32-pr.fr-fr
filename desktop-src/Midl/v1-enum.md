---
title: v1_enum (attribut)
description: L’attribut \ v1 \_ enum \ indique que le type énuméré spécifié doit être transmis en tant qu’entité 32 bits, plutôt que la valeur par défaut 16 bits.
ms.assetid: 46016131-b78e-4a7f-94c8-41ff1780b0b8
keywords:
- v1_enum MIDL de l’attribut
topic_type:
- apiref
api_name:
- v1_enum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8183b8b91c4a061e6b91c67ab83bca6393751f4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841322"
---
# <a name="v1_enum-attribute"></a><span data-ttu-id="df6b0-104">\_attribut enum v1</span><span class="sxs-lookup"><span data-stu-id="df6b0-104">v1\_enum attribute</span></span>

<span data-ttu-id="df6b0-105">L’attribut **\[ \_ enum \] v1** indique que le type énuméré spécifié doit être transmis en tant qu’entité 32 bits, plutôt que la valeur par défaut 16 bits.</span><span class="sxs-lookup"><span data-stu-id="df6b0-105">The **\[v1\_enum\]** attribute directs that the specified enumerated type be transmitted as a 32-bit entity, rather than the 16-bit default.</span></span>

``` syntax
[v1_enum] enum 
{
    ...
};
```

## <a name="parameters"></a><span data-ttu-id="df6b0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="df6b0-106">Parameters</span></span>

<span data-ttu-id="df6b0-107">Cet attribut n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="df6b0-107">This attribute has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="df6b0-108">Notes</span><span class="sxs-lookup"><span data-stu-id="df6b0-108">Remarks</span></span>

<span data-ttu-id="df6b0-109">L’utilisation de l’attribut **\[ \_ enum \] v1** pour transmettre un type énuméré en tant qu’entité 32 bits augmente l’efficacité du marshaling et du démarshaling des données lorsqu’une telle énumération est incorporée dans les structures ou les unions.</span><span class="sxs-lookup"><span data-stu-id="df6b0-109">Using the **\[v1\_enum\]** attribute to transmit an enumerated type as a 32-bit entity increases the efficiency of marshaling and unmarshaling data when such an enumeration is embedded in structures or unions.</span></span>

<span data-ttu-id="df6b0-110">Pour améliorer les performances, nous vous recommandons d’appliquer l’attribut **\[ \_ enum \] v1** aux énumérateurs dans les applications 32 bits.</span><span class="sxs-lookup"><span data-stu-id="df6b0-110">For improved performance, we recommend applying the **\[v1\_enum\]** attribute to enumerators in 32-bit applications.</span></span> <span data-ttu-id="df6b0-111">Gardez toutefois à l’esprit que sur les plateformes 16 bits, le compilateur C traite un type énuméré comme un [**entier**](int.md)16 bits. Par conséquent, les applications clientes 16 bits doivent convertir les types [**enum**](enum.md) en [**long**](long.md) pour la transmission à distance afin d’éviter de remplacer les données ou d’envoyer des valeurs incorrectes.</span><span class="sxs-lookup"><span data-stu-id="df6b0-111">Keep in mind, however, that on 16-bit platforms the C compiler treats an enumerated type as a 16-bit [**int**](int.md). Therefore 16-bit client applications need to convert [**enum**](enum.md) types to [**long**](long.md) for remote transmission in order to avoid overwriting data or sending incorrect values.</span></span>

## <a name="examples"></a><span data-ttu-id="df6b0-112">Exemples</span><span class="sxs-lookup"><span data-stu-id="df6b0-112">Examples</span></span>

``` syntax
typedef [v1_enum] enum 
{
    value1, 
    value2, ...
};
```

## <a name="see-also"></a><span data-ttu-id="df6b0-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df6b0-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df6b0-114">**variables**</span><span class="sxs-lookup"><span data-stu-id="df6b0-114">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="df6b0-115">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="df6b0-115">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="df6b0-116">**long**</span><span class="sxs-lookup"><span data-stu-id="df6b0-116">**long**</span></span>](long.md)
</dt> </dl>

 

 




