---
description: La commande suivante encapsule un certificat X. 509, MyCert. cer, dans un test de \# certificat d’éditeur de logiciel PKCS 7 (SPC), appelé MyCert. spc.
ms.assetid: c3287289-d2bf-4d1d-80f0-e7dd41a3cbe3
title: Utilisation de Cert2SPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fca10b0ab121e283a181c84b056b63ce10ece385
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527621"
---
# <a name="using-cert2spc"></a><span data-ttu-id="949b8-103">Utilisation de Cert2SPC</span><span class="sxs-lookup"><span data-stu-id="949b8-103">Using Cert2SPC</span></span>

<span data-ttu-id="949b8-104">La commande suivante encapsule un certificat [*X. 509*](../secgloss/x-gly.md) , *myCert*. cer, dans un test de \# [*certificat d’éditeur de logiciel*](../secgloss/s-gly.md) PKCS 7 (SPC), appelé *myCert*. spc.</span><span class="sxs-lookup"><span data-stu-id="949b8-104">The following command wraps an [*X.509*](../secgloss/x-gly.md) certificate, *MyCert*.cer, into a test PKCS \#7 [*Software Publisher Certificate*](../secgloss/s-gly.md) (SPC), called *MyCert*.spc.</span></span> <span data-ttu-id="949b8-105">Le SPC créé doit être utilisé à des fins de test uniquement.</span><span class="sxs-lookup"><span data-stu-id="949b8-105">The SPC created is to be used for test purposes only.</span></span> <span data-ttu-id="949b8-106">Un SPC utilisé pour signer le code à distribuer au public doit être obtenu auprès de GTE, VeriSign, Inc., ou d’une autre [*autorité de certification*](../secgloss/c-gly.md) approuvée.</span><span class="sxs-lookup"><span data-stu-id="949b8-106">An SPC used to actually sign code to be distributed to the public must be obtained from GTE, VeriSign, Inc., or another trusted [*certification authority*](../secgloss/c-gly.md) (CA).</span></span>

<span data-ttu-id="949b8-107">**Cert2spc** \*myCert \* \* *. cer* \*  *myCert \* \* *. spc**</span><span class="sxs-lookup"><span data-stu-id="949b8-107">**Cert2SPC** *MyCert\*\*\*.cer*\* *MyCert\*\*\*.spc*\*</span></span>

 

 
