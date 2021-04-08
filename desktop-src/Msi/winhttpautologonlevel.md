---
description: La stratégie de connexion automatique (ouverture de session automatique) détermine le moment où il est acceptable pour WinHTTP d’inclure les informations d’identification par défaut dans une demande au serveur.
ms.assetid: 4ED8B6BC-E52D-4DE9-A9AE-1FDF61A978A9
title: WinHttpAutoLogonLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7760faa94e24b7fe5b33717c504b03e4de42c0aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866053"
---
# <a name="winhttpautologonlevel"></a><span data-ttu-id="a4c25-103">WinHttpAutoLogonLevel</span><span class="sxs-lookup"><span data-stu-id="a4c25-103">WinHttpAutoLogonLevel</span></span>

<span data-ttu-id="a4c25-104">La stratégie de connexion automatique (ouverture de session automatique) détermine le moment où il est acceptable pour *WinHTTP* d’inclure les informations d’identification par défaut dans une demande au serveur.</span><span class="sxs-lookup"><span data-stu-id="a4c25-104">The automatic logon (auto-logon) policy determines when it is acceptable for *WinHTTP* to include the default credentials in a request to the server.</span></span>

<span data-ttu-id="a4c25-105">Vous pouvez définir cette valeur sur **L** pour le niveau de sécurité le plus bas du niveau de **\_ \_ sécurité \_ \_ WinHTTP**, définir sur **M** **pour \_ \_ \_ \_ le** niveau de sécurité de l'  ouverture de la configuration de l' **\_ ouverture \_ \_ \_** de</span><span class="sxs-lookup"><span data-stu-id="a4c25-105">You can set this value to **L** for **WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_LOW**, set to **M** for **WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_MEDIUM**, and set to **H** for **WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_HIGH**.</span></span> <span data-ttu-id="a4c25-106">Le niveau par défaut est **WinHTTP \_ Autologon \_ niveau de sécurité \_ \_ moyen**.</span><span class="sxs-lookup"><span data-stu-id="a4c25-106">The default level is **WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_MEDIUM**.</span></span> <span data-ttu-id="a4c25-107">Pour plus d’informations sur la stratégie de connexion automatique, consultez la section relative à [l’authentification dans WinHTTP](../winhttp/authentication-in-winhttp.md).</span><span class="sxs-lookup"><span data-stu-id="a4c25-107">For more information about automatic logon policy, see the section for [Authentication in WinHTTP](../winhttp/authentication-in-winhttp.md).</span></span>

<span data-ttu-id="a4c25-108">**Windows 8 et Windows Server 2012 :** Cette stratégie requiert Windows Installer s’exécutant sur Windows 8 ou Windows Server 2012 et n’est pas disponible sur toutes les versions antérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="a4c25-108">**Windows 8 and Windows Server 2012:** This policy requires Windows Installer running on the Windows 8 or Windows Server 2012 and is unavailable on all earlier versions of Windows.</span></span>

## <a name="registry-key"></a><span data-ttu-id="a4c25-109">Clé de Registre</span><span class="sxs-lookup"><span data-stu-id="a4c25-109">Registry Key</span></span>

<span data-ttu-id="a4c25-110">**HKEY \_ \_** \\ **Stratégies logicielles** de l’ordinateur local \\  \\ **Microsoft** \\ **Windows** \\ **installer**</span><span class="sxs-lookup"><span data-stu-id="a4c25-110">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="a4c25-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="a4c25-111">Data Type</span></span>

<span data-ttu-id="a4c25-112">**SZ de REG \_**</span><span class="sxs-lookup"><span data-stu-id="a4c25-112">**REG\_SZ**</span></span>

 

 
