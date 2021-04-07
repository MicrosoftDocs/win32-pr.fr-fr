---
title: Codes d’erreur Win32 pour ADSI
description: Les codes d’erreur Win32 standard sont également utilisés pour retourner des messages d’erreur ADSI.
ms.assetid: 5b7b85c9-ccca-4ea3-8b37-54f6b30a509f
ms.tgt_platform: multiple
keywords:
- Codes d’erreur Win32 pour ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a47151a3a1619a7f224dc0b9b7f0871813a346a3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671098"
---
# <a name="win32-error-codes-for-adsi"></a><span data-ttu-id="e2968-104">Codes d’erreur Win32 pour ADSI</span><span class="sxs-lookup"><span data-stu-id="e2968-104">Win32 Error Codes for ADSI</span></span>

<span data-ttu-id="e2968-105">Les codes d’erreur Win32 standard sont également utilisés pour retourner des messages d’erreur ADSI.</span><span class="sxs-lookup"><span data-stu-id="e2968-105">Standard Win32 error codes are also used to return ADSI error messages.</span></span> <span data-ttu-id="e2968-106">Plus précisément, le fournisseur LDAP ADSI mappe tous les codes d’erreur LDAP aux codes d’erreur Win32.</span><span class="sxs-lookup"><span data-stu-id="e2968-106">Specifically, the ADSI LDAP provider maps all the LDAP error codes to Win32 error codes.</span></span> <span data-ttu-id="e2968-107">Les valeurs **HRESULT** de ces codes d’erreur sont au format 0x8007XXXX, où les quatre derniers chiffres hexadécimaux, XXXX, correspondent aux valeurs **DWORD** du code d’erreur Win32 approprié.</span><span class="sxs-lookup"><span data-stu-id="e2968-107">The **HRESULT** values of these error codes are of the 0x8007XXXX format, where the last four hexadecimal digits, XXXX, corresponds to the **DWORD** values of the appropriate Win32 error code.</span></span> <span data-ttu-id="e2968-108">Par exemple, la valeur d’erreur ADSI 0x80072020 donne la valeur d’erreur Win32 0x2020 au format hexadécimal ou 8224 en notation décimale.</span><span class="sxs-lookup"><span data-stu-id="e2968-108">For example, the ADSI error value 0x80072020 gives the Win32 error value of 0x2020 in hexadecimal or 8224 in decimal.</span></span>

<span data-ttu-id="e2968-109">Pour convertir la valeur **HRESULT** d’un code d’erreur ADSI, retourné par votre application, en la valeur **DWORD** de l’erreur Win32 correspondante, telle que définie dans les fichiers d’en-tête ci-dessus, utilisez la procédure suivante.</span><span class="sxs-lookup"><span data-stu-id="e2968-109">To convert the **HRESULT** value of an ADSI error code, returned by your application, to the corresponding the Win32 error **DWORD** value, as defined in the header files above, use the following procedure.</span></span>

<span data-ttu-id="e2968-110">La plupart des codes d’erreur Win32 pour ADSI sont définis dans Winerror. h ou Lmerr. h.</span><span class="sxs-lookup"><span data-stu-id="e2968-110">Most of the Win32 error codes for ADSI are defined in Winerror.h or Lmerr.h.</span></span> <span data-ttu-id="e2968-111">Les valeurs d’erreur sont répertoriées sous forme de valeurs décimales dans ces fichiers.</span><span class="sxs-lookup"><span data-stu-id="e2968-111">The error values are listed as decimal values in these files.</span></span>

<span data-ttu-id="e2968-112">**Pour convertir la valeur **HRESULT** d’un code d’erreur ADSI en la valeur **DWORD** Win32 Error correspondante**</span><span class="sxs-lookup"><span data-stu-id="e2968-112">**To convert the **HRESULT** value of an ADSI error code to the corresponding the Win32 error **DWORD** value**</span></span>

1.  <span data-ttu-id="e2968-113">Convertit la valeur **HRESULT** en nombre hexadécimal si vous commencez par une valeur décimale, comme vous pouvez l’obtenir à partir d’une application de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="e2968-113">Convert the **HRESULT** value to a hexadecimal number if starting with a decimal value as you may get from a Visual Basic application.</span></span>
2.  <span data-ttu-id="e2968-114">Déposez la partie 0x8007 pour produire le reste.</span><span class="sxs-lookup"><span data-stu-id="e2968-114">Drop the 0x8007 part produce the remainder.</span></span>
3.  <span data-ttu-id="e2968-115">Convertit le reste en nombre décimal.</span><span class="sxs-lookup"><span data-stu-id="e2968-115">Convert the remainder to a decimal number.</span></span>
4.  <span data-ttu-id="e2968-116">Recherchez le reste de la valeur décimale dans Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="e2968-116">Look up the decimal remainder in Winerror.h.</span></span>
5.  <span data-ttu-id="e2968-117">S’il est introuvable dans Winerror. h, soustraire 2100 du reste décimal et recherchez le résultat dans Lmerr. h.</span><span class="sxs-lookup"><span data-stu-id="e2968-117">If not found in Winerror.h, subtract 2100 from the decimal remainder and look up the result in Lmerr.h.</span></span>

<span data-ttu-id="e2968-118">ADSI 2,0 mappe les codes d’erreur LDAP à un ensemble de codes d’erreur Win32 qui est différent de celui utilisé dans ADSI pour Windows 2000 et le client DS.</span><span class="sxs-lookup"><span data-stu-id="e2968-118">ADSI 2.0 maps the LDAP error codes to a set of Win32 error codes that is different from that used in ADSI for Windows 2000 and DS Client.</span></span> <span data-ttu-id="e2968-119">Les différences sont répertoriées dans :</span><span class="sxs-lookup"><span data-stu-id="e2968-119">The differences are listed in:</span></span>

-   [<span data-ttu-id="e2968-120">Codes d’erreur Win32</span><span class="sxs-lookup"><span data-stu-id="e2968-120">Win32 Error Codes</span></span>](win32-error-codes.md)
-   [<span data-ttu-id="e2968-121">Codes d’erreur Win32 pour ADSI 2,0</span><span class="sxs-lookup"><span data-stu-id="e2968-121">Win32 Error Codes for ADSI 2.0</span></span>](win32-error-codes-for-adsi-2-0.md)

 

 




