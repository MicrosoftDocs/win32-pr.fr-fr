---
description: 'En savoir plus sur : définition de la prise en forme PPP par défaut pour un processus'
title: Définition de la reconnaissance par défaut des PPP pour un processus (Windows)
TOCTitle: Setting the default DPI awareness for a process
ms:assetid: C9488338-D863-45DF-B5CB-7ED9B869A5E2
ms:mtpsurl: https://msdn.microsoft.com/library/Mt846517(v=VS.85)
ms:contentKeyID: 74520139
ms.date: 03/30/2018
ms.topic: article
mtps_version: v=VS.85
ms.openlocfilehash: c9192bf650588b7c21f17afb45149fe460f91bea
ms.sourcegitcommit: ecd0ba4732f5264aab9baa2839c11f7fea36318f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/07/2021
ms.locfileid: "113481864"
---
# <a name="setting-the-default-dpi-awareness-for-a-process"></a><span data-ttu-id="35d37-103">Définition de la reconnaissance par défaut des PPP pour un processus</span><span class="sxs-lookup"><span data-stu-id="35d37-103">Setting the default DPI awareness for a process</span></span>

<span data-ttu-id="35d37-104">les applications de bureau sur Windows peuvent s’exécuter dans différents modes de reconnaissance ppp.</span><span class="sxs-lookup"><span data-stu-id="35d37-104">Desktop applications on Windows can run in different DPI awareness modes.</span></span> <span data-ttu-id="35d37-105">Ces modes activent différents comportements de mise à l’échelle DPI et peuvent utiliser des espaces de coordonnées différents.</span><span class="sxs-lookup"><span data-stu-id="35d37-105">These modes enable different DPI scaling behavior and can use different coordinate spaces.</span></span> <span data-ttu-id="35d37-106">Pour plus d’informations sur la reconnaissance DPI, consultez [développement d’applications bureautiques haute résolution sur Windows.](https://msdn.microsoft.com/library/mt843498\(v=vs.85\))</span><span class="sxs-lookup"><span data-stu-id="35d37-106">For more information on DPI awareness, see [High DPI Desktop Application Development on Windows.](https://msdn.microsoft.com/library/mt843498\(v=vs.85\))</span></span> <span data-ttu-id="35d37-107">Il est important de définir explicitement le mode de reconnaissance PPP par défaut de votre processus afin d’éviter tout comportement inattendu.</span><span class="sxs-lookup"><span data-stu-id="35d37-107">It is important that you explicitly set the default DPI awareness mode of your process so as to avoid unexpected behavior.</span></span>

<span data-ttu-id="35d37-108">Il existe deux méthodes principales pour spécifier la prise en compte des PPP par défaut d’un processus :</span><span class="sxs-lookup"><span data-stu-id="35d37-108">There are two main methods to specify the default DPI awareness of a process:</span></span>

<span data-ttu-id="35d37-109">1 \) via un paramètre du manifeste d’application</span><span class="sxs-lookup"><span data-stu-id="35d37-109">1\) through an application manifest setting</span></span>

<span data-ttu-id="35d37-110">2 par \) programmation à l’aide d’un appel d’API</span><span class="sxs-lookup"><span data-stu-id="35d37-110">2\) programmatically through an API call</span></span>

<span data-ttu-id="35d37-111">Nous vous recommandons de spécifier la reconnaissance par défaut des PPP de processus via un paramètre de manifeste.</span><span class="sxs-lookup"><span data-stu-id="35d37-111">We recommended that you specify the default process DPI awareness via a manifest setting.</span></span> <span data-ttu-id="35d37-112">Si la spécification de l’API par défaut via est prise en charge, elle n’est pas recommandée.</span><span class="sxs-lookup"><span data-stu-id="35d37-112">While specifying the default via API is supported, it is not recommended.</span></span>

## <a name="setting-default-awareness-with-the-application-manifest"></a><span data-ttu-id="35d37-113">Définition de la sensibilisation par défaut au manifeste d’application</span><span class="sxs-lookup"><span data-stu-id="35d37-113">Setting default awareness with the application manifest</span></span>

<span data-ttu-id="35d37-114">Il existe deux paramètres de manifeste qui vous permettent de spécifier le mode de reconnaissance PPP par défaut du processus : \<dpiAwareness\> et \<dpiAware\> .</span><span class="sxs-lookup"><span data-stu-id="35d37-114">There are two manifest settings that enable you to specify the process default DPI awareness mode: \<dpiAwareness\> and \<dpiAware\>.</span></span> <span data-ttu-id="35d37-115">\<dpiAware\>a été introduite dans Windows Vista et permet uniquement de définir la reconnaissance du système par défaut de votre processus.</span><span class="sxs-lookup"><span data-stu-id="35d37-115">\<dpiAware\> was introduced in Windows Vista and only enables your process default to be set to system awareness.</span></span> <span data-ttu-id="35d37-116">\<dpiAwareness\>a été introduite dans Windows 10, version 1607 et vous permet de spécifier une liste triée de modes de reconnaissance des ppp par défaut de processus.</span><span class="sxs-lookup"><span data-stu-id="35d37-116">\<dpiAwareness\> was introduced in Windows 10, version 1607 and enables you to specify an ordered list of process-default DPI awareness modes.</span></span> <span data-ttu-id="35d37-117">cela vous permet de définir les modes de reconnaissance ppp de sauvegarde, qui seront utilisés si votre application est exécutée sur une version de Windows ne peut pas prendre en charge le premier mode de sensibilisation spécifié.</span><span class="sxs-lookup"><span data-stu-id="35d37-117">This enables you to set backup DPI awareness modes, which will be used if your application is ran on a version of Windows unable to support the first awareness mode specified.</span></span> <span data-ttu-id="35d37-118">dans les versions antérieures de Windows, la \<dpiAwareness\> balise la plus récente sera ignorée.</span><span class="sxs-lookup"><span data-stu-id="35d37-118">On older versions of Windows, the newer \<dpiAwareness\> tag will be ignored.</span></span> <span data-ttu-id="35d37-119">cela signifie que vous pouvez utiliser ces deux paramètres de manifeste pour activer un scénario dans lequel la valeur par défaut du processus peut être la reconnaissance du système sur une version antérieure de Windows tout en étant Per-Monitor sur les versions supérieures à Windows 10, version 1607.</span><span class="sxs-lookup"><span data-stu-id="35d37-119">This means that you can use both of these manifest settings to enable a scenario where your process default could be system awareness on older version of Windows while being Per-Monitor on versions greater than Windows 10, version 1607.</span></span> <span data-ttu-id="35d37-120">sur Windows 10, la version 1607 et la valeur on, le \<dpiAware\> paramètre est ignoré si l' \<dpiAwareness\> élément est présent.</span><span class="sxs-lookup"><span data-stu-id="35d37-120">On Windows 10, version 1607, and on, the \<dpiAware\> setting is ignored if the \<dpiAwareness\> element is present.</span></span>

<span data-ttu-id="35d37-121">Le tableau ci-dessous montre comment spécifier des modes de reconnaissance des PPP par défaut de processus différents à l’aide des deux paramètres de manifeste :</span><span class="sxs-lookup"><span data-stu-id="35d37-121">The table below shows how to specify different process-default DPI awareness modes using the two manifest settings:</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="35d37-122">Traiter le mode de reconnaissance PPP par défaut</span><span class="sxs-lookup"><span data-stu-id="35d37-122">Process default DPI awareness mode</span></span></th>
<th><span data-ttu-id="35d37-123">&lt;&gt;paramètre dpiAware</span><span class="sxs-lookup"><span data-stu-id="35d37-123">&lt;dpiAware&gt; setting</span></span></th>
<th><span data-ttu-id="35d37-124">&lt;&gt;paramètre dpiAwareness (Windows 10, version 1607 et versions ultérieures)</span><span class="sxs-lookup"><span data-stu-id="35d37-124">&lt;dpiAwareness&gt; setting (Windows 10, version 1607 and later)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="35d37-125">ignore</span><span class="sxs-lookup"><span data-stu-id="35d37-125">unaware</span></span></td>
<td><p><span data-ttu-id="35d37-126">N/A (aucun paramètre dpiAware dans le manifeste)</span><span class="sxs-lookup"><span data-stu-id="35d37-126">N/A (no dpiAware setting in manifest)</span></span></p>
<p><span data-ttu-id="35d37-127">ou</span><span class="sxs-lookup"><span data-stu-id="35d37-127">or</span></span></p>
<p><span data-ttu-id="35d37-128">&lt;dpiAware &gt; false &lt; /dpiAware&gt;</span><span class="sxs-lookup"><span data-stu-id="35d37-128">&lt;dpiAware&gt;false&lt;/dpiAware&gt;</span></span></p></td>
<td><span data-ttu-id="35d37-129">&lt;dpiAwareness ne &gt; connaissant pas &lt; /dpiAwareness&gt;</span><span class="sxs-lookup"><span data-stu-id="35d37-129">&lt;dpiAwareness&gt;unaware&lt;/dpiAwareness&gt;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35d37-130">Prise en charge par le système</span><span class="sxs-lookup"><span data-stu-id="35d37-130">System aware</span></span></td>
<td><span data-ttu-id="35d37-131">&lt;dpiAware &gt; true &lt; /dpiAware&gt;</span><span class="sxs-lookup"><span data-stu-id="35d37-131">&lt;dpiAware&gt;true&lt;/dpiAware&gt;</span></span></td>
<td><span data-ttu-id="35d37-132">&lt;dpiAwareness &gt; système &lt; /dpiAwareness&gt;</span><span class="sxs-lookup"><span data-stu-id="35d37-132">&lt;dpiAwareness&gt;system&lt;/dpiAwareness&gt;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="35d37-133">Par moniteur</span><span class="sxs-lookup"><span data-stu-id="35d37-133">Per Monitor</span></span></td>
<td><span data-ttu-id="35d37-134">&lt;dpiAware &gt; true/PM &lt; dpiAware&gt;</span><span class="sxs-lookup"><span data-stu-id="35d37-134">&lt;dpiAware&gt;true/pm&lt;dpiAware&gt;</span></span></td>
<td><span data-ttu-id="35d37-135">&lt;dpiAwareness &gt; permonitor &lt; /dpiAwareness&gt;</span><span class="sxs-lookup"><span data-stu-id="35d37-135">&lt;dpiAwareness&gt;PerMonitor&lt;/dpiAwareness&gt;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35d37-136">Par moniteur v2</span><span class="sxs-lookup"><span data-stu-id="35d37-136">Per Monitor V2</span></span></td>
<td><span data-ttu-id="35d37-137">Non prise en charge</span><span class="sxs-lookup"><span data-stu-id="35d37-137">Not supported</span></span></td>
<td><span data-ttu-id="35d37-138">&lt;dpiAwareness &gt; PerMonitorV2 &lt; /dpiAwareness&gt;</span><span class="sxs-lookup"><span data-stu-id="35d37-138">&lt;dpiAwareness&gt;PerMonitorV2&lt;/dpiAwareness&gt;</span></span></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="35d37-139">L’exemple ci-dessous montre à la fois les \<dpiAwareness\> \<dpiAware\> paramètres et utilisés dans le même fichier manifeste pour configurer le comportement de reconnaissance dpi par défaut du processus pour les différentes versions de Windows.</span><span class="sxs-lookup"><span data-stu-id="35d37-139">The sample below shows both the \<dpiAwareness\> and the \<dpiAware\> settings being used within the same manifest file to configure process-default DPI awareness behavior for different versions of Windows.</span></span>

```xml
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
  <asmv3:application>
    <asmv3:windowsSettings>
      <dpiAware xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">true</dpiAware>
      <dpiAwareness xmlns="http://schemas.microsoft.com/SMI/2016/WindowsSettings">PerMonitorV2</dpiAwareness>
    </asmv3:windowsSettings>
  </asmv3:application>
</assembly>
```

## <a name="setting-default-awareness-programmatically"></a><span data-ttu-id="35d37-140">Définition par programmation de la sensibilisation par défaut</span><span class="sxs-lookup"><span data-stu-id="35d37-140">Setting default awareness programmatically</span></span>

<span data-ttu-id="35d37-141">Bien qu’il ne soit pas recommandé, il est possible de définir la reconnaissance par défaut des PPP par défaut.</span><span class="sxs-lookup"><span data-stu-id="35d37-141">Although it is not recommended, it is possible to set the default DPI awareness programmatically.</span></span> <span data-ttu-id="35d37-142">Une fois qu’une fenêtre (HWND) a été créée dans votre processus, la modification du mode de reconnaissance PPP n’est plus prise en charge.</span><span class="sxs-lookup"><span data-stu-id="35d37-142">Once a window (an HWND) has been created in your process, changing the DPI awareness mode is no longer supported.</span></span> <span data-ttu-id="35d37-143">Si vous définissez le mode de prise en forme des PPP par défaut du processus par programme, vous devez appeler l’API correspondante avant la création de tous les HWND.</span><span class="sxs-lookup"><span data-stu-id="35d37-143">If you are setting the process-default DPI awareness mode programmatically, you must call the corresponding API before any HWNDs have been created.</span></span>

<span data-ttu-id="35d37-144">Il existe plusieurs API qui vous permettent de spécifier la prise en compte des PPP par défaut pour votre processus.</span><span class="sxs-lookup"><span data-stu-id="35d37-144">There are multiple APIs that let you specify the default DPI awareness for your process.</span></span> <span data-ttu-id="35d37-145">L’API actuellement recommandée est [**SetProcessDpiAwarenessContext**](https://msdn.microsoft.com/library/mt807676\(v=vs.85\)), car les anciennes API offrent moins de fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="35d37-145">The current recommended API is [**SetProcessDpiAwarenessContext**](https://msdn.microsoft.com/library/mt807676\(v=vs.85\)), as older APIs offer less functionality.</span></span>

 

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="35d37-146">API</span><span class="sxs-lookup"><span data-stu-id="35d37-146">API</span></span></th>
<th><span data-ttu-id="35d37-147">Version minimale de Windows</span><span class="sxs-lookup"><span data-stu-id="35d37-147">Minimum version of Windows</span></span></th>
<th><span data-ttu-id="35d37-148">Prise en charge de DPI</span><span class="sxs-lookup"><span data-stu-id="35d37-148">DPI Unaware</span></span></th>
<th><span data-ttu-id="35d37-149">Prise en charge DPI système</span><span class="sxs-lookup"><span data-stu-id="35d37-149">System DPI Aware</span></span></th>
<th><span data-ttu-id="35d37-150">Prise en charge DPI par moniteur</span><span class="sxs-lookup"><span data-stu-id="35d37-150">Per Monitor DPI Aware</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="35d37-151"><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiaware">SetProcessDPIAware</a></span><span class="sxs-lookup"><span data-stu-id="35d37-151"><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiaware">SetProcessDPIAware</a></span></span></td>
<td><span data-ttu-id="35d37-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="35d37-152">Windows Vista</span></span></td>
<td><span data-ttu-id="35d37-153">N/A</span><span class="sxs-lookup"><span data-stu-id="35d37-153">N/A</span></span></td>
<td><span data-ttu-id="35d37-154">SetProcessDPIAware()</span><span class="sxs-lookup"><span data-stu-id="35d37-154">SetProcessDPIAware()</span></span></td>
<td><span data-ttu-id="35d37-155">N/A</span><span class="sxs-lookup"><span data-stu-id="35d37-155">N/A</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35d37-156"><a href="/windows/win32/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness"><strong>SetProcessDpiAwareness</strong></a></span><span class="sxs-lookup"><span data-stu-id="35d37-156"><a href="/windows/win32/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness"><strong>SetProcessDpiAwareness</strong></a></span></span></td>
<td><span data-ttu-id="35d37-157">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="35d37-157">Windows 8.1</span></span></td>
<td><span data-ttu-id="35d37-158">SetProcessDpiAwareness (PROCESS_DPI_UNAWARE)</span><span class="sxs-lookup"><span data-stu-id="35d37-158">SetProcessDpiAwareness(PROCESS_DPI_UNAWARE)</span></span></td>
<td><span data-ttu-id="35d37-159">SetProcessDpiAwareness (PROCESS_SYSTEM_DPI_AWARE)</span><span class="sxs-lookup"><span data-stu-id="35d37-159">SetProcessDpiAwareness(PROCESS_SYSTEM_DPI_AWARE)</span></span></td>
<td><span data-ttu-id="35d37-160">SetProcessDpiAwareness (PROCESS_PER_MONITOR_DPI_AWARE)</span><span class="sxs-lookup"><span data-stu-id="35d37-160">SetProcessDpiAwareness(PROCESS_PER_MONITOR_DPI_AWARE)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="35d37-161"><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiawarenesscontext"><strong>SetProcessDpiAwarenessContext</strong></a></span><span class="sxs-lookup"><span data-stu-id="35d37-161"><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiawarenesscontext"><strong>SetProcessDpiAwarenessContext</strong></a></span></span></td>
<td><span data-ttu-id="35d37-162">Windows 10, version 1607</span><span class="sxs-lookup"><span data-stu-id="35d37-162">Windows 10, version 1607</span></span></td>
<td><span data-ttu-id="35d37-163">SetProcessDpiAwarenessContext (DPI_AWARENESS_CONTEXT_UNAWARE)</span><span class="sxs-lookup"><span data-stu-id="35d37-163">SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_UNAWARE)</span></span></td>
<td><span data-ttu-id="35d37-164">SetProcessDpiAwarenessContext (DPI_AWARENESS_CONTEXT_SYSTEM_AWARE)</span><span class="sxs-lookup"><span data-stu-id="35d37-164">SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_SYSTEM_AWARE)</span></span></td>
<td><p><span data-ttu-id="35d37-165">SetProcessDpiAwarenessContext (DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE)</span><span class="sxs-lookup"><span data-stu-id="35d37-165">SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE)</span></span></p>
<p><span data-ttu-id="35d37-166">SetProcessDpiAwarenessContext (DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2)</span><span class="sxs-lookup"><span data-stu-id="35d37-166">SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2)</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="process-default-vs-thread-default"></a><span data-ttu-id="35d37-167">Processus-par défaut par rapport au thread par défaut</span><span class="sxs-lookup"><span data-stu-id="35d37-167">Process-default vs. Thread default</span></span>

<span data-ttu-id="35d37-168">Ce document fait référence à la définition de la prise en face PPP par défaut pour votre processus.</span><span class="sxs-lookup"><span data-stu-id="35d37-168">This document refers to setting the default DPI awareness for your process.</span></span> <span data-ttu-id="35d37-169">cela est dû au fait que Windows 10 a introduit la prise en charge de l’exécution de plusieurs modes de reconnaissance dpi au sein d’un même processus (avant Windows 10, l’ensemble du processus devait se conformer à un seul mode de reconnaissance ppp).</span><span class="sxs-lookup"><span data-stu-id="35d37-169">This is because Windows 10 introduced support for running more than one DPI awareness mode within a single process (prior to Windows 10, the entire process had to conform to a single DPI awareness mode).</span></span> <span data-ttu-id="35d37-170">La prise en charge de l’exécution de plusieurs modes de reconnaissance DPI au sein d’un processus est appelée « mise à l’échelle DPI en mode mixte ».</span><span class="sxs-lookup"><span data-stu-id="35d37-170">Support for running more than one DPI awareness mode within a process is referred to as "mixed-mode DPI scaling".</span></span> <span data-ttu-id="35d37-171">Lors de l’utilisation de la mise à l’échelle DPI en mode mixte au sein de votre processus, chaque fenêtre de niveau supérieur peut s’exécuter dans un mode de reconnaissance PPP qui peut être différent de celui de la valeur par défaut du processus.</span><span class="sxs-lookup"><span data-stu-id="35d37-171">When using mixed-mode DPI scaling within your process, each top-level Window can run in a DPI awareness mode that may be different than that of the process default.</span></span> <span data-ttu-id="35d37-172">Sauf spécification explicite, chaque thread utilise par défaut le processus par défaut lors de sa création.</span><span class="sxs-lookup"><span data-stu-id="35d37-172">Unless explicitly specified, each thread will default to the process default when created.</span></span> <span data-ttu-id="35d37-173">Pour plus d’informations sur la mise à l’échelle DPI en mode mixte, reportez-vous à l’article sur la mise à l' [échelle dpi en mode mixte](https://msdn.microsoft.com/library/mt744321\(v=vs.85\)) .</span><span class="sxs-lookup"><span data-stu-id="35d37-173">For more information about mixed-mode DPI scaling, refer to the [Mixed-Mode DPI Scaling](https://msdn.microsoft.com/library/mt744321\(v=vs.85\)) article.</span></span>
