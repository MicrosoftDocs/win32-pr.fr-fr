---
title: Codes d’erreur LDAP pour ADSI
description: Lorsqu’un serveur LDAP génère une erreur et transmet l’erreur au client, l’erreur est ensuite convertie en chaîne par le client LDAP.
ms.assetid: 7a0a5a1b-8473-405b-a590-3f917e50cbdc
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 149abf4562b0e35067149fb69c9a1ec1304cc528
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839169"
---
# <a name="ldap-error-codes-for-adsi"></a><span data-ttu-id="fbb34-103">Codes d’erreur LDAP pour ADSI</span><span class="sxs-lookup"><span data-stu-id="fbb34-103">LDAP Error Codes for ADSI</span></span>

<span data-ttu-id="fbb34-104">Lorsqu’un serveur LDAP génère une erreur et transmet l’erreur au client, l’erreur est ensuite convertie en chaîne par le client LDAP.</span><span class="sxs-lookup"><span data-stu-id="fbb34-104">When an LDAP server generates an error and passes the error to the client, the error is then translated into a string by the LDAP client.</span></span>

<span data-ttu-id="fbb34-105">Cette méthode est similaire aux [codes d’erreur Win32 pour ADSI](win32-error-codes-for-adsi.md).</span><span class="sxs-lookup"><span data-stu-id="fbb34-105">This method is similar to [Win32 error codes for ADSI](win32-error-codes-for-adsi.md).</span></span> <span data-ttu-id="fbb34-106">Dans cet exemple, le code d’erreur du client est l’erreur WIN32 0x80072020.</span><span class="sxs-lookup"><span data-stu-id="fbb34-106">In this example, the client error code is the WIN32 error 0x80072020.</span></span>

<span data-ttu-id="fbb34-107">**Pour déterminer les codes d’erreur LDAP pour ADSI**</span><span class="sxs-lookup"><span data-stu-id="fbb34-107">**To Determine the LDAP error codes for ADSI**</span></span>

1.  <span data-ttu-id="fbb34-108">Supprimez 8007 du code d’erreur WIN32.</span><span class="sxs-lookup"><span data-stu-id="fbb34-108">Drop the 8007 from the WIN32 error code.</span></span> <span data-ttu-id="fbb34-109">Dans l’exemple, la valeur hexadécimale restante est 2020.</span><span class="sxs-lookup"><span data-stu-id="fbb34-109">In the example, the remaining hex value is 2020.</span></span>
2.  <span data-ttu-id="fbb34-110">Convertit la valeur hexadécimale restante en valeur décimale.</span><span class="sxs-lookup"><span data-stu-id="fbb34-110">Convert the remaining hex value to a decimal value.</span></span> <span data-ttu-id="fbb34-111">Dans l’exemple, la valeur hexadécimale restante 2020 est convertie en valeur décimale 8224.</span><span class="sxs-lookup"><span data-stu-id="fbb34-111">In the example, the remaining hex value 2020 converts to the decimal value 8224.</span></span>
3.  <span data-ttu-id="fbb34-112">Dans le fichier WinError. h, recherchez la définition de la valeur décimale.</span><span class="sxs-lookup"><span data-stu-id="fbb34-112">Search in the WinError.h file for the definition of the decimal value.</span></span> <span data-ttu-id="fbb34-113">Dans l’exemple, 8224L correspond à l’erreur erreur erreurs du **\_ service d’annuaire \_ \_**.</span><span class="sxs-lookup"><span data-stu-id="fbb34-113">In the example, 8224L corresponds to the error **ERROR\_DS\_OPERATIONS\_ERROR**.</span></span>
4.  <span data-ttu-id="fbb34-114">Remplacez le préfixe **Error \_ DS** par **LDAP \_**.</span><span class="sxs-lookup"><span data-stu-id="fbb34-114">Replace the prefix **ERROR\_DS** with **LDAP\_**.</span></span> <span data-ttu-id="fbb34-115">Dans l’exemple, la nouvelle définition est **\_ \_ erreur LDAP Operations**.</span><span class="sxs-lookup"><span data-stu-id="fbb34-115">In the example, the new definition is **LDAP\_OPERATIONS\_ERROR**.</span></span>
5.  <span data-ttu-id="fbb34-116">Dans le fichier Winldap. h, recherchez la valeur de la définition de l’erreur LDAP.</span><span class="sxs-lookup"><span data-stu-id="fbb34-116">Search in the Winldap.h file for the value of the LDAP error definition.</span></span> <span data-ttu-id="fbb34-117">Dans l’exemple, la valeur de **l' \_ \_ erreur opérations LDAP** dans le fichier Winldap. h est 0x01.</span><span class="sxs-lookup"><span data-stu-id="fbb34-117">In the example, the value of **LDAP\_OPERATIONS\_ERROR** in the Winldap.h file is 0x01.</span></span>

 

 




