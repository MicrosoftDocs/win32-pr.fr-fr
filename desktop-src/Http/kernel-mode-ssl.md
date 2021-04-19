---
title: SSL en mode noyau
description: SSL en mode noyau
ms.assetid: ada82704-cb7d-4e98-8c87-76c7bfbd098b
keywords:
- SSL en mode noyau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 737ac7c6c25bac6e7b66d91aa967fc6fa550459b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106513691"
---
# <a name="kernel-mode-ssl"></a><span data-ttu-id="ecadc-104">SSL en mode noyau</span><span class="sxs-lookup"><span data-stu-id="ecadc-104">Kernel Mode SSL</span></span>

<span data-ttu-id="ecadc-105">Le mode noyau SSL a été introduit dans Windows Server 2003 avec Service Pack 1 (SP1) avec prise en charge limitée.</span><span class="sxs-lookup"><span data-stu-id="ecadc-105">Kernel mode SSL was introduced in Windows Server 2003 with Service Pack 1 (SP1) with limited support.</span></span> <span data-ttu-id="ecadc-106">Pour les ordinateurs qui exécutent Windows Server 2003 avec SP1, une clé de registre doit être configurée pour activer le SSL de noyau.</span><span class="sxs-lookup"><span data-stu-id="ecadc-106">For computers running on Windows Server 2003 with SP1 a registry key must be set to enable kernel SSL.</span></span> <span data-ttu-id="ecadc-107">Pour les ordinateurs qui exécutent Windows Server 2008 et Windows Vista, la prise en charge du mode noyau complet pour SSL est fournie.</span><span class="sxs-lookup"><span data-stu-id="ecadc-107">For computers running on Windows Server 2008 and Windows Vista, full kernel mode support for SSL is provided.</span></span>

<span data-ttu-id="ecadc-108">Les sections suivantes décrivent la prise en charge SSL en mode noyau :</span><span class="sxs-lookup"><span data-stu-id="ecadc-108">The following sections describe kernel mode SSL support:</span></span>

-   <span data-ttu-id="ecadc-109">Modes noyau SSL dans Windows Server 2003 avec SP1</span><span class="sxs-lookup"><span data-stu-id="ecadc-109">Kernel Modes SSL in Windows Server 2003 with SP1</span></span>
-   <span data-ttu-id="ecadc-110">SSL en mode noyau dans Windows Server 2008 et Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ecadc-110">Kernel Mode SSL in Windows Server 2008 and Windows Vista</span></span>

## <a name="kernel-modes-ssl-in-windows-server-2003-with-sp1"></a><span data-ttu-id="ecadc-111">Modes noyau SSL dans Windows Server 2003 avec SP1</span><span class="sxs-lookup"><span data-stu-id="ecadc-111">Kernel Modes SSL in Windows Server 2003 with SP1</span></span>

<span data-ttu-id="ecadc-112">Dans Windows Server 2003 avec SP1, l’API du serveur HTTP offre la possibilité d’exécuter la sécurité SSL en mode noyau (le mode utilisateur est SSL par défaut).</span><span class="sxs-lookup"><span data-stu-id="ecadc-112">In Windows Server 2003 with SP1, HTTP Server API provides the option of running SSL security in kernel mode (user mode SSL is the default).</span></span> <span data-ttu-id="ecadc-113">La fonctionnalité en mode noyau améliore les performances SSL en déplaçant les opérations de chiffrement et de déchiffrement vers le noyau, réduisant ainsi le nombre de transitions entre le mode noyau et le mode utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ecadc-113">The kernel mode feature improves SSL performance by moving encryption and decryption operations to the kernel, thus reducing the number of transitions between kernel mode and user mode.</span></span>

<span data-ttu-id="ecadc-114">Les fonctionnalités suivantes ne sont pas prises en charge lorsque SSL est exécuté en mode noyau :</span><span class="sxs-lookup"><span data-stu-id="ecadc-114">The following features are not supported when SSL is run in kernel mode:</span></span>

-   <span data-ttu-id="ecadc-115">Certificats clients</span><span class="sxs-lookup"><span data-stu-id="ecadc-115">Client certificates</span></span>
-   <span data-ttu-id="ecadc-116">Chiffrements RC2</span><span class="sxs-lookup"><span data-stu-id="ecadc-116">RC2 ciphers</span></span>
-   <span data-ttu-id="ecadc-117">Le protocole PCT 1,0</span><span class="sxs-lookup"><span data-stu-id="ecadc-117">The PCT 1.0 protocol</span></span>
-   <span data-ttu-id="ecadc-118">Les modifications de configuration de certificat de serveur requièrent un redémarrage du service HTTP</span><span class="sxs-lookup"><span data-stu-id="ecadc-118">Server certificate configuration changes require a restart of the HTTP service</span></span>
-   <span data-ttu-id="ecadc-119">Chiffrement en bloc et prise en charge du déchargement</span><span class="sxs-lookup"><span data-stu-id="ecadc-119">Bulk encryption and offload support</span></span>

## <a name="configuring-kernel-mode-ssl"></a><span data-ttu-id="ecadc-120">Configuration du mode noyau SSL</span><span class="sxs-lookup"><span data-stu-id="ecadc-120">Configuring Kernel Mode SSL</span></span>

<span data-ttu-id="ecadc-121">Le mode noyau SSL est contrôlé par la valeur de Registre **EnableKernelSSL** et est activé en définissant la valeur sur 1.</span><span class="sxs-lookup"><span data-stu-id="ecadc-121">Kernel mode SSL is controlled by the **EnableKernelSSL** registry value and is enabled by setting the value to 1.</span></span> <span data-ttu-id="ecadc-122">L’activation du mode noyau SSL désactive le mode utilisateur SSL et nécessite le redémarrage du service HTTP pour prendre effet.</span><span class="sxs-lookup"><span data-stu-id="ecadc-122">Enabling kernel mode SSL will disable user mode SSL and requires the HTTP service to be restarted to take effect.</span></span> <span data-ttu-id="ecadc-123">La clé de Registre **EnableKernelSSL** se trouve à l’emplacement suivant :</span><span class="sxs-lookup"><span data-stu-id="ecadc-123">The **EnableKernelSSL** registry key is located at:</span></span>

<span data-ttu-id="ecadc-124">**HKEY \_ \_** \\  \\  \\  \\  \\ **Paramètres** http des services \\  de CurrentControlSet de système d’ordinateur local EnableKernelSSL</span><span class="sxs-lookup"><span data-stu-id="ecadc-124">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**HTTP**\\**Parameters**\\**EnableKernelSSL**</span></span>

## <a name="kernel-mode-ssl-in-windows-server-2008-and-windows-vista"></a><span data-ttu-id="ecadc-125">SSL en mode noyau dans Windows Server 2008 et Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ecadc-125">Kernel Mode SSL in Windows Server 2008 and Windows Vista</span></span>

<span data-ttu-id="ecadc-126">Pour les ordinateurs qui exécutent Windows Server 2008 et Windows Vista, l’API du serveur HTTP offre des fonctionnalités SSL améliorées.</span><span class="sxs-lookup"><span data-stu-id="ecadc-126">For computers running on Windows Server 2008 and Windows Vista, the HTTP Server API features enhanced SSL functionality.</span></span>

<span data-ttu-id="ecadc-127">Les nouvelles fonctionnalités suivantes sont prises en charge :</span><span class="sxs-lookup"><span data-stu-id="ecadc-127">The following new features are supported:</span></span>

-   <span data-ttu-id="ecadc-128">Prise en charge complète des certificats clients en mode noyau SSL</span><span class="sxs-lookup"><span data-stu-id="ecadc-128">Full client certificate support in kernel mode SSL</span></span>
-   <span data-ttu-id="ecadc-129">SSL en mode noyau pour toutes les transactions HTTP SSL</span><span class="sxs-lookup"><span data-stu-id="ecadc-129">Kernel mode SSL for all HTTP SSL transactions</span></span>
-   <span data-ttu-id="ecadc-130">Chiffrement en bloc et prise en charge du déchargement</span><span class="sxs-lookup"><span data-stu-id="ecadc-130">Bulk encryption and offload support</span></span>
-   <span data-ttu-id="ecadc-131">Le protocole PCT 1,0</span><span class="sxs-lookup"><span data-stu-id="ecadc-131">The PCT 1.0 protocol</span></span>
-   <span data-ttu-id="ecadc-132">Chiffrements RC2</span><span class="sxs-lookup"><span data-stu-id="ecadc-132">RC2 ciphers</span></span>
-   <span data-ttu-id="ecadc-133">Performances accrues par rapport au mode utilisateur SSL</span><span class="sxs-lookup"><span data-stu-id="ecadc-133">Increased performance over user mode SSL</span></span>

## <a name="configuration"></a><span data-ttu-id="ecadc-134">Configuration</span><span class="sxs-lookup"><span data-stu-id="ecadc-134">Configuration</span></span>

<span data-ttu-id="ecadc-135">Le mode noyau SSL peut être configuré à l’aide de deux valeurs de Registre sous la clé des paramètres HTTP, à l’emplacement suivant :</span><span class="sxs-lookup"><span data-stu-id="ecadc-135">Kernel mode SSL is configurable through two registry values under the HTTP Parameters key located at:</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            HTTP
               Parameters
                  EnableSslCloseNotify
                  DisableSslCertChainCacheOnlyUrlRetrieval
```

<span data-ttu-id="ecadc-136">Un utilisateur doit disposer des privilèges administrateur/système local pour modifier les valeurs de Registre et afficher ou modifier les fichiers journaux et le dossier qui les contient.</span><span class="sxs-lookup"><span data-stu-id="ecadc-136">A user must have Administrator/Local System privileges to modify the registry values and view, or modify, the log files and the folder that contains them.</span></span>

<span data-ttu-id="ecadc-137">Les informations de configuration dans les valeurs de Registre sont lues lorsque le pilote de l’API du serveur HTTP est démarré.</span><span class="sxs-lookup"><span data-stu-id="ecadc-137">Configuration information in the registry values is read when the HTTP Server API driver is started.</span></span> <span data-ttu-id="ecadc-138">Par conséquent, si les paramètres sont modifiés, le pilote doit être arrêté et redémarré pour lire les nouvelles valeurs.</span><span class="sxs-lookup"><span data-stu-id="ecadc-138">As a result, if the settings are changed the driver must be stopped and restarted to read the new values.</span></span> <span data-ttu-id="ecadc-139">Pour ce faire, vous pouvez utiliser les commandes de console suivantes :</span><span class="sxs-lookup"><span data-stu-id="ecadc-139">This can be accomplished by using the following console commands:</span></span>

<span data-ttu-id="ecadc-140">**net stop http**</span><span class="sxs-lookup"><span data-stu-id="ecadc-140">**net stop http**</span></span>

<span data-ttu-id="ecadc-141">**NET START http**</span><span class="sxs-lookup"><span data-stu-id="ecadc-141">**net start http**</span></span>

<span data-ttu-id="ecadc-142">Le tableau suivant répertorie les valeurs de configuration du Registre.</span><span class="sxs-lookup"><span data-stu-id="ecadc-142">The following table lists registry configuration values.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ecadc-143">Valeur de Registre</span><span class="sxs-lookup"><span data-stu-id="ecadc-143">Registry Value</span></span></th>
<th><span data-ttu-id="ecadc-144">Description</span><span class="sxs-lookup"><span data-stu-id="ecadc-144">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ecadc-145">EnableKernelSSL</span><span class="sxs-lookup"><span data-stu-id="ecadc-145">EnableKernelSSL</span></span></td>
<td><span data-ttu-id="ecadc-146"><strong>Windows Server 2008 et Windows Vista :</strong> Cette valeur de Registre est obsolète.</span><span class="sxs-lookup"><span data-stu-id="ecadc-146"><strong>Windows Server 2008 and Windows Vista:</strong> This registry value is obsolete.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ecadc-147">EnableSslCloseNotify</span><span class="sxs-lookup"><span data-stu-id="ecadc-147">EnableSslCloseNotify</span></span></td>
<td><span data-ttu-id="ecadc-148">Valeur <strong>DWORD</strong> qui a la valeur <strong>true</strong> pour activer Close-Notify ou <strong>false</strong> pour désactiver la spécification de fermeture-notification.</span><span class="sxs-lookup"><span data-stu-id="ecadc-148">A <strong>DWORD</strong> value that is set to <strong>TRUE</strong> to enable close-notify, or <strong>FALSE</strong> to disable the close-notify requirement.</span></span> <span data-ttu-id="ecadc-149">Fermer-Notify est désactivé par défaut.</span><span class="sxs-lookup"><span data-stu-id="ecadc-149">Close-notify is disabled by default.</span></span><br/> <span data-ttu-id="ecadc-150">Lorsque l’option fermer-notifier est activée, l’application cliente est requise pour envoyer un message de fermeture et de notification avant de fermer les connexions TCP.</span><span class="sxs-lookup"><span data-stu-id="ecadc-150">When close-notify is enabled, the client application is required to send a close-notify message before closing TCP connections.</span></span> <span data-ttu-id="ecadc-151">L’API du serveur HTTP envoie également une notification de fermeture avant de fermer la connexion.</span><span class="sxs-lookup"><span data-stu-id="ecadc-151">The HTTP Server API also sends a close-notify before closing the connection.</span></span><br/> <span data-ttu-id="ecadc-152">Lorsque l’option fermer-notifier est activée et que le client envoie un message de fermeture-notification, l’API du serveur HTTP réutilise la session SSL sur les connexions futures au client.</span><span class="sxs-lookup"><span data-stu-id="ecadc-152">When close-notify is enabled, and the client sends a close-notify message, the HTTP Server API will reuse the SSL session on future connections to the client.</span></span> <span data-ttu-id="ecadc-153">Si le client n’envoie pas de fermeture-notification, l’API du serveur HTTP ne réutilisera pas la même session SSL sur les connexions futures.</span><span class="sxs-lookup"><span data-stu-id="ecadc-153">If the client does not send a close-notify, the HTTP Server API will not reuse the same SSL session on future connections.</span></span> <span data-ttu-id="ecadc-154">Par conséquent, une liaison SSL complète est déclenchée sur la nouvelle connexion, ce qui réduit les performances.</span><span class="sxs-lookup"><span data-stu-id="ecadc-154">Thus, a full SSL handshake is triggered on the new connection thereby reducing performance.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="ecadc-155">L’activation de la fonction de fermeture-notification permet d’atténuer les attaques par troncation contre les requêtes et les réponses HTTPs.</span><span class="sxs-lookup"><span data-stu-id="ecadc-155">Enabling close-notify helps mitigate truncation attacks against the HTTPS requests and responses.</span></span>
</blockquote>
<br/> <br/> <span data-ttu-id="ecadc-156">Lorsque la fermeture-notification est désactivée, l’API du serveur HTTP réutilise la session SSL pour les connexions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ecadc-156">When close-notify is disabled, the HTTP Server API reuses the SSL session for future connections.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ecadc-157">DisableSslCertChainCacheOnlyUrlRetrieval</span><span class="sxs-lookup"><span data-stu-id="ecadc-157">DisableSslCertChainCacheOnlyUrlRetrieval</span></span></td>
<td><span data-ttu-id="ecadc-158">Valeur <strong>DWORD</strong> définie sur <strong>true</strong> pour permettre à l’API du serveur http de récupérer des certificats intermédiaires à partir d’Internet ou du magasin local, ou <strong>false</strong> pour récupérer des certificats intermédiaires du magasin local uniquement.</span><span class="sxs-lookup"><span data-stu-id="ecadc-158">A <strong>DWORD</strong> value that is set to <strong>TRUE</strong> to enable the HTTP Server API to retrieve intermediate certificates from either the Internet, or the local store, or <strong>FALSE</strong> to retrieve intermediate certificates from the local store only.</span></span> <span data-ttu-id="ecadc-159">La valeur de Registre par défaut est <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="ecadc-159">The default registry value is <strong>FALSE</strong>.</span></span><br/> <span data-ttu-id="ecadc-160">Par défaut, l’API du serveur HTTP crée une chaîne de certificats client en récupérant les certificats intermédiaires dans le magasin de l’autorité de certification intermédiaire sous le compte de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="ecadc-160">By default, the HTTP Server API builds a client certificate chain by retrieving the intermediate certificates from the Intermediate Certificate Authority store under the local machine account.</span></span> <span data-ttu-id="ecadc-161">Si cette valeur est définie sur <strong>true</strong> , l’API du serveur http récupère les certificats intermédiaires non seulement dans le magasin local, mais également à partir de l’autorité de certification intermédiaire sur Internet.</span><span class="sxs-lookup"><span data-stu-id="ecadc-161">Setting this value to <strong>TRUE</strong> enables the HTTP Server API to retrieve the intermediate certificates not only from the local store, but also from the Intermediate Certificate Authority on the Internet.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 





