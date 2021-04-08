---
description: Crypt32.dll est le module qui implémente la plupart des fonctions CryptoAPI.
ms.assetid: b6063c92-5831-4b78-b2cd-812e55194bc9
title: Versions de Crypt32.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71b55d78b3ff3654e4bf3e5956917dd8de20eec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750924"
---
# <a name="crypt32dll-versions"></a><span data-ttu-id="37866-103">Versions de Crypt32.dll</span><span class="sxs-lookup"><span data-stu-id="37866-103">Crypt32.dll Versions</span></span>

<span data-ttu-id="37866-104">Crypt32.dll est le module qui implémente un grand nombre des fonctions de certificat et de messagerie de chiffrement dans l’CryptoAPI, telles que [**CryptSignMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage).</span><span class="sxs-lookup"><span data-stu-id="37866-104">Crypt32.dll is the module that implements many of the Certificate and Cryptographic Messaging functions in the CryptoAPI, such as [**CryptSignMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage).</span></span> <span data-ttu-id="37866-105">Crypt32.dll est un module fourni avec les systèmes d’exploitation Windows et Windows Server, mais les différentes versions de cette DLL offrent des fonctionnalités différentes.</span><span class="sxs-lookup"><span data-stu-id="37866-105">Crypt32.dll is a module that comes with the Windows and Windows Server operating systems, but different versions of this DLL provide different capabilities.</span></span> <span data-ttu-id="37866-106">Il n’existe aucune API pour déterminer la version de CryptoAPI en cours d’utilisation, mais vous pouvez déterminer la version de Crypt32.dll en cours d’utilisation à l’aide des fonctions [**GetFileVersionInfo**](/windows/win32/api/winver/nf-winver-getfileversioninfoa) et [**VerQueryValue**](/windows/win32/api/winver/nf-winver-verqueryvaluea) .</span><span class="sxs-lookup"><span data-stu-id="37866-106">There is no API to determine the version of CryptoAPI that is in use, but you can determine the version of Crypt32.dll that is currently in use by using the [**GetFileVersionInfo**](/windows/win32/api/winver/nf-winver-getfileversioninfoa) and [**VerQueryValue**](/windows/win32/api/winver/nf-winver-verqueryvaluea) functions.</span></span>

<span data-ttu-id="37866-107">En général, les plages de versions de Crypt32.dll correspondent aux versions de système d’exploitation, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="37866-107">In general, the version ranges of Crypt32.dll map to the operating system versions as shown in the following table.</span></span> <span data-ttu-id="37866-108">Toutefois, cette table doit être utilisée comme indication uniquement parce qu’il est possible, par le biais d’autres moyens de mise à jour, que la version du Crypt32.dll diffère de celle indiquée dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="37866-108">However, this table should be used as a guideline only because it is possible, through other update avenues, that the Crypt32.dll version will differ from the one indicated in the table.</span></span>

| <span data-ttu-id="37866-109">Version de Crypt32.dll</span><span class="sxs-lookup"><span data-stu-id="37866-109">Crypt32.dll version</span></span>                               | <span data-ttu-id="37866-110">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="37866-110">Operating system</span></span>                                                                                                                                                                |
|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37866-111">*version* >= 5.131.3790.0</span><span class="sxs-lookup"><span data-stu-id="37866-111">*version* >= 5.131.3790.0</span></span>                      | <span data-ttu-id="37866-112">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="37866-112">Windows Server 2003</span></span>                                                                                                                                                             |
| <span data-ttu-id="37866-113">*version* >= 5.131.2600.1243</span><span class="sxs-lookup"><span data-stu-id="37866-113">*version* >= 5.131.2600.1243</span></span>                   | <span data-ttu-id="37866-114">Windows XP avec Service Pack 2 (SP2) Windows XP avec Service Pack 1 (SP1) avec correctif [Q329433](https://support.microsoft.com/kb/329433)</span><span class="sxs-lookup"><span data-stu-id="37866-114">Windows XP with Service Pack 2 (SP2)Windows XP with Service Pack 1 (SP1) with hotfix [Q329433](https://support.microsoft.com/kb/329433)</span></span><br/> <span data-ttu-id="37866-115">Windows XP</span><span class="sxs-lookup"><span data-stu-id="37866-115">Windows XP</span></span><br/> |
| <span data-ttu-id="37866-116">5.131.2600.0 <= *version* < 5.131.2600.1243</span><span class="sxs-lookup"><span data-stu-id="37866-116">5.131.2600.0 <= *version* < 5.131.2600.1243</span></span> | <span data-ttu-id="37866-117">Windows XP avec SP1Windows XP</span><span class="sxs-lookup"><span data-stu-id="37866-117">Windows XP with SP1Windows XP</span></span><br/>                                                                                                                                        |



 

 

 
