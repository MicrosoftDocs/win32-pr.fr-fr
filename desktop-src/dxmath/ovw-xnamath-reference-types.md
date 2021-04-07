---
description: La bibliothèque DirectXMath fournit un certain nombre de structures et de types définis pour encapsuler les données afin de prendre en charge la facilité d’utilisation, l’optimisation et la portabilité.
ms.assetid: 4b9ffc17-3917-551c-7cb5-19de505dfd21
title: Types de bibliothèque DirectXMath
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32ac888e451fe1e1ba5cfc66184bf2eb7b6feffd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863485"
---
# <a name="directxmath-library-types"></a><span data-ttu-id="dd173-103">Types de bibliothèque DirectXMath</span><span class="sxs-lookup"><span data-stu-id="dd173-103">DirectXMath Library types</span></span>

<span data-ttu-id="dd173-104">La bibliothèque DirectXMath fournit un certain nombre de structures et de types définis pour encapsuler les données afin de prendre en charge la facilité d’utilisation, l’optimisation et la portabilité.</span><span class="sxs-lookup"><span data-stu-id="dd173-104">The DirectXMath Library provides a number of structures and defined types to encapsulate data to support ease of use, optimization, and portability.</span></span>

<span data-ttu-id="dd173-105">La liste ci-dessous comprend des structures qui font actuellement partie de la bibliothèque DirectXMath et sont disponibles via l’en-tête DirectXMath. h.</span><span class="sxs-lookup"><span data-stu-id="dd173-105">The list below includes structures currently part of the DirectXMath Library, and available through the DirectXMath.h header.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="dd173-106">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="dd173-106">In this section</span></span>



| <span data-ttu-id="dd173-107">Rubrique</span><span class="sxs-lookup"><span data-stu-id="dd173-107">Topic</span></span>                                                             | <span data-ttu-id="dd173-108">Description</span><span class="sxs-lookup"><span data-stu-id="dd173-108">Description</span></span>                                                                                                                                                                       |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dd173-109">**DEMI-type de données**</span><span class="sxs-lookup"><span data-stu-id="dd173-109">**HALF Data Type**</span></span>](half-data-type.md)<br/>               | <span data-ttu-id="dd173-110">Alias de **UInt16 \_ t** compressé avec un nombre à virgule flottante de 16 bits constitué d’un bit de signe, d’un exposant biaisé à 5 bits et d’une mantisse 10 bits.</span><span class="sxs-lookup"><span data-stu-id="dd173-110">An alias to **uint16\_t** packed with a 16-bit floating-point number consisting of a sign bit, a 5-bit biased exponent, and a 10-bit mantissa.</span></span><br/>                         |
| [<span data-ttu-id="dd173-111">**Type de données XMVECTOR**</span><span class="sxs-lookup"><span data-stu-id="dd173-111">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)<br/>       | <span data-ttu-id="dd173-112">Type portable utilisé pour représenter un vecteur de composants à virgule flottante ou entier 4 32 bits, chacun étant aligné de manière optimale et mappé à un registre de vecteur matériel.</span><span class="sxs-lookup"><span data-stu-id="dd173-112">A portable type used to represent a vector of four 32-bit floating-point or integer components, each aligned optimally and mapped to a hardware vector register.</span></span><br/>       |
| [<span data-ttu-id="dd173-113">**Type de données XMVECTORF32**</span><span class="sxs-lookup"><span data-stu-id="dd173-113">**XMVECTORF32 Data Type**</span></span>](xmvectorf32-data-type.md)<br/> | <span data-ttu-id="dd173-114">Type portable opaque pour prendre en charge l’utilisation de la syntaxe d’initialiseur C/C++ pour charger des valeurs à virgule flottante dans une instance de type [**XMVECTOR**](xmvector-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="dd173-114">An opaque, portable type to support the use of C/C++ initializer syntax to load floating-point values into an instance of [**XMVECTOR**](xmvector-data-type.md) type.</span></span><br/> |
| [<span data-ttu-id="dd173-115">**Type de données XMVECTORI32**</span><span class="sxs-lookup"><span data-stu-id="dd173-115">**XMVECTORI32 Data Type**</span></span>](xmvectori32-data-type.md)<br/> | <span data-ttu-id="dd173-116">Type portable opaque pour prendre en charge l’utilisation de la syntaxe d’initialiseur C/C++ pour charger des valeurs entières dans une instance de type [**XMVECTOR**](xmvector-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="dd173-116">An opaque, portable type to support the use of C/C++ initializer syntax to load integer values into an instance of [**XMVECTOR**](xmvector-data-type.md) type.</span></span><br/>        |
| [<span data-ttu-id="dd173-117">**Type de données XMVECTORU32**</span><span class="sxs-lookup"><span data-stu-id="dd173-117">**XMVECTORU32 Data Type**</span></span>](xmvectoru32-data-type.md)<br/> | <span data-ttu-id="dd173-118">Type portable opaque pour prendre en charge l’utilisation de la syntaxe d’initialiseur C/C++ pour charger les \_ valeurs UInt32 t dans une instance de type XMVECTOR.</span><span class="sxs-lookup"><span data-stu-id="dd173-118">An opaque, portable type to support the use of C/C++ initializer syntax to load uint32\_t values into an instance of XMVECTOR type.</span></span><br/>                                    |
| [<span data-ttu-id="dd173-119">**Type de données XMVECTORU8**</span><span class="sxs-lookup"><span data-stu-id="dd173-119">**XMVECTORU8 Data Type**</span></span>](xmvectoru8-data-type.md)<br/>   | <span data-ttu-id="dd173-120">Type portable opaque pour prendre en charge l’utilisation de la syntaxe d’initialiseur C/C++ pour charger les valeurs de UInt8 \_ t dans une instance de type XMVECTOR.</span><span class="sxs-lookup"><span data-stu-id="dd173-120">An opaque, portable type to support the use of C/C++ initializer syntax to load uint8\_t values into an instance of XMVECTOR type.</span></span><br/>                                     |



 

## <a name="related-topics"></a><span data-ttu-id="dd173-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dd173-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd173-122">Informations de référence sur la programmation DirectXMath</span><span class="sxs-lookup"><span data-stu-id="dd173-122">DirectXMath Programming Reference</span></span>](ovw-xnamath-reference.md)
</dt> </dl>

 

 




