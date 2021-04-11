---
description: Les informations contenues dans cette rubrique s’appliquent à Windows Server 2003 et Windows XP.
ms.assetid: 45536902-af80-4dca-b3ce-207086844763
title: Protocole SSL (Secure Sockets Layer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3ed2555c854a6cc25948abe0dc83043ee632170
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951882"
---
# <a name="secure-sockets-layer-protocol"></a><span data-ttu-id="0561a-103">Protocole SSL (Secure Sockets Layer)</span><span class="sxs-lookup"><span data-stu-id="0561a-103">Secure Sockets Layer Protocol</span></span>

<span data-ttu-id="0561a-104">Les informations contenues dans cette rubrique s’appliquent à Windows Server 2003 et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0561a-104">The information in this topic applies to Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="0561a-105">Pour les suites de chiffrement pour Windows Server 2008 et Windows Vista, voir [suites de chiffrement dans Schannel](cipher-suites-in-schannel.md).</span><span class="sxs-lookup"><span data-stu-id="0561a-105">For cipher suites for Windows Server 2008 and Windows Vista, see [Cipher Suites in Schannel](cipher-suites-in-schannel.md).</span></span>

<span data-ttu-id="0561a-106">Schannel prend en charge les versions 2,0 et 3,0 du [*protocole SSL (Secure Sockets Layer) (SSL)*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="0561a-106">Schannel supports versions 2.0 and 3.0 of the [*Secure Sockets Layer (SSL) protocol*](../secgloss/s-gly.md).</span></span>

> [!Note]  
> <span data-ttu-id="0561a-107">À partir de Windows 10, version 1607 et Windows Server 2016, SSL 2,0 a été supprimé et n’est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="0561a-107">Beginning with Windows 10, version 1607 and Windows Server 2016, SSL 2.0 has been removed and is no longer supported.</span></span>

 

## <a name="ssl-30"></a><span data-ttu-id="0561a-108">SSL 3.0</span><span class="sxs-lookup"><span data-stu-id="0561a-108">SSL 3.0</span></span>

<span data-ttu-id="0561a-109">SSL 3,0 est le prédécesseur du [protocole TLS (Transport Layer Security](transport-layer-security-protocol.md)).</span><span class="sxs-lookup"><span data-stu-id="0561a-109">SSL 3.0 is the predecessor of the [Transport Layer Security Protocol](transport-layer-security-protocol.md).</span></span>

<span data-ttu-id="0561a-110">Schannel prend en charge les suites de chiffrement listées sous [suites de chiffrement TLS](tls-cipher-suites.md) pour SSL 3,0.</span><span class="sxs-lookup"><span data-stu-id="0561a-110">Schannel supports the cipher suites listed under [TLS Cipher Suites](tls-cipher-suites.md) for SSL 3.0.</span></span> <span data-ttu-id="0561a-111">SSL 3,0 prend en charge toutes les suites de chiffrement listées sous les suites de chiffrement TLS, ainsi que les \_ Kea Fortezza SSL \_ \_ avec \_ Fortezza \_ CBC \_ Sha.</span><span class="sxs-lookup"><span data-stu-id="0561a-111">SSL 3.0 supports all of the cipher suites listed under TLS Cipher Suites as well as SSL\_FORTEZZA\_KEA\_WITH\_FORTEZZA\_CBC\_SHA.</span></span>

## <a name="ssl-20"></a><span data-ttu-id="0561a-112">SSL 2.0</span><span class="sxs-lookup"><span data-stu-id="0561a-112">SSL 2.0</span></span>

<span data-ttu-id="0561a-113">SSL 2,0 a été remplacé par TLS et ne doit pas être utilisé pour un nouveau développement.</span><span class="sxs-lookup"><span data-stu-id="0561a-113">SSL 2.0 has been superseded by TLS and should not be used for new development.</span></span>

<span data-ttu-id="0561a-114">Schannel prend en charge les suites de chiffrement suivantes pour SSL 2,0.</span><span class="sxs-lookup"><span data-stu-id="0561a-114">Schannel supports the following cipher suites for SSL 2.0.</span></span> <span data-ttu-id="0561a-115">Les suites sont répertoriées dans l’ordre, de la plus sécurisée à la moins sécurisée.</span><span class="sxs-lookup"><span data-stu-id="0561a-115">The suites are listed in order from most secure to least secure.</span></span>

-   <span data-ttu-id="0561a-116">SSL \_ RC4 \_ 128 \_ avec \_ MD5</span><span class="sxs-lookup"><span data-stu-id="0561a-116">SSL\_RC4\_128\_WITH\_MD5</span></span>
-   <span data-ttu-id="0561a-117">SSL \_ des \_ 192 \_ EDE3 \_ CBC \_ avec \_ MD5</span><span class="sxs-lookup"><span data-stu-id="0561a-117">SSL\_DES\_192\_EDE3\_CBC\_WITH\_MD5</span></span>
-   <span data-ttu-id="0561a-118">SSL \_ RC2 \_ CBC \_ 128 \_ CBC \_ avec \_ MD5</span><span class="sxs-lookup"><span data-stu-id="0561a-118">SSL\_RC2\_CBC\_128\_CBC\_WITH\_MD5</span></span>
-   <span data-ttu-id="0561a-119">SSL \_ des \_ 64 \_ CBC \_ avec \_ MD5</span><span class="sxs-lookup"><span data-stu-id="0561a-119">SSL\_DES\_64\_CBC\_WITH\_MD5</span></span>
-   <span data-ttu-id="0561a-120">SSL \_ RC4 \_ 128 \_ EXPORT40 \_ avec \_ MD5</span><span class="sxs-lookup"><span data-stu-id="0561a-120">SSL\_RC4\_128\_EXPORT40\_WITH\_MD5</span></span>

 

 
