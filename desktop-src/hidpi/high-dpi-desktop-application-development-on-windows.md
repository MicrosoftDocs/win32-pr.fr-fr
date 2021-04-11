---
title: Développement d’applications de bureau haute résolution sur Windows
description: Ce contenu est destiné aux développeurs qui cherchent à mettre à jour les applications de bureau pour gérer le facteur d’échelle d’affichage dynamique (également appelé
ms.assetid: 6C419EEF-D898-4B50-8D16-E65A594487AA
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7af4a7a1d65077838dfa65f7cf89dee475a0b4dc
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2020
ms.locfileid: "104102485"
---
# <a name="high-dpi-desktop-application-development-on-windows"></a><span data-ttu-id="09d2d-103">Développement d’applications de bureau haute résolution sur Windows</span><span class="sxs-lookup"><span data-stu-id="09d2d-103">High DPI Desktop Application Development on Windows</span></span>

<span data-ttu-id="09d2d-104">Ce contenu est destiné aux développeurs qui cherchent à mettre à jour les applications de bureau pour gérer les modifications du facteur d’échelle d’affichage (points par pouce ou PPP) de manière dynamique, ce qui permet à leurs applications d’être nettes sur n’importe quel affichage sur lequel elles sont affichées.</span><span class="sxs-lookup"><span data-stu-id="09d2d-104">This content is targeted at developers who are looking to update desktop applications to handle display scale factor (dots per inch, or DPI) changes dynamically, allowing their applications to be crisp on any display they're rendered on.</span></span>

<span data-ttu-id="09d2d-105">Pour commencer, si vous créez une nouvelle application Windows à partir de zéro, il est fortement recommandé de créer une application [plateforme Windows universelle (UWP)](/windows/uwp/get-started/whats-a-uwp) .</span><span class="sxs-lookup"><span data-stu-id="09d2d-105">To start, if you're creating a new Windows app from scratch, it is highly recommended that you create a [Universal Windows Platform (UWP)](/windows/uwp/get-started/whats-a-uwp) application.</span></span> <span data-ttu-id="09d2d-106">Les applications UWP sont &mdash; mises à l’échelle de manière automatique et dynamique &mdash; pour chaque affichage sur lequel elles s’exécutent.</span><span class="sxs-lookup"><span data-stu-id="09d2d-106">UWP applications automatically&mdash;and dynamically&mdash;scale for each display that they're running on.</span></span>

<span data-ttu-id="09d2d-107">Les applications de bureau utilisant des technologies de programmation Windows plus anciennes (programmation Win32 brute, Windows Forms, WPF (Windows Presentation Framework), etc.) ne peuvent pas gérer automatiquement la mise à l’échelle DPI sans travail supplémentaire du développeur.</span><span class="sxs-lookup"><span data-stu-id="09d2d-107">Desktop applications using older Windows programming technologies (raw Win32 programming, Windows Forms, Windows Presentation Framework (WPF), etc.) are unable to automatically handle DPI scaling without additional developer work.</span></span> <span data-ttu-id="09d2d-108">Sans ce travail, les applications apparaissent floues ou de taille incorrecte dans de nombreux scénarios d’utilisation courants.</span><span class="sxs-lookup"><span data-stu-id="09d2d-108">Without such work, applications will appear blurry or incorrectly-sized in many common usage scenarios.</span></span> <span data-ttu-id="09d2d-109">Ce document fournit un contexte et des informations sur ce qui est impliqué dans la mise à jour d’une application de bureau pour un rendu correct.</span><span class="sxs-lookup"><span data-stu-id="09d2d-109">This document provides context and information about what is involved in updating a desktop application to render correctly.</span></span>

## <a name="display-scale-factor--dpi"></a><span data-ttu-id="09d2d-110">Afficher le facteur d’échelle & PPP</span><span class="sxs-lookup"><span data-stu-id="09d2d-110">Display Scale Factor & DPI</span></span>

<span data-ttu-id="09d2d-111">À mesure que la technologie d’affichage progresse, les fabricants de panneaux d’affichage ont compressé un nombre grandissant de pixels dans chaque unité d’espace physique sur leurs panneaux.</span><span class="sxs-lookup"><span data-stu-id="09d2d-111">As display technology has progressed, display panel manufacturers have packed an increasing number of pixels into each unit of physical space on their panels.</span></span> <span data-ttu-id="09d2d-112">Cela a entraîné une augmentation des points par pouce (DPI) des panneaux d’affichage modernes plus hauts qu’ils n’ont été historiquement.</span><span class="sxs-lookup"><span data-stu-id="09d2d-112">This has resulted in the dots per inch (DPI) of modern display panels being much higher than they have historically been.</span></span> <span data-ttu-id="09d2d-113">Dans le passé, la plupart des affichages contenait 96 pixels par pouce linéaire de l’espace physique (96 ppp); dans 2017, les affichages de près de 300 ppp ou plus sont facilement disponibles.</span><span class="sxs-lookup"><span data-stu-id="09d2d-113">In the past, most displays had 96 pixels per linear inch of physical space (96 DPI); in 2017, displays with nearly 300 DPI or higher are readily available.</span></span>

<span data-ttu-id="09d2d-114">La plupart des infrastructures d’interface utilisateur de bureau héritées ont des hypothèses intégrées que la résolution d’affichage ne changera pas pendant la durée de vie du processus.</span><span class="sxs-lookup"><span data-stu-id="09d2d-114">Most legacy desktop UI frameworks have built-in assumptions that the display DPI will not change during the lifetime of the process.</span></span>  <span data-ttu-id="09d2d-115">Cette hypothèse n’est plus vraie, avec les DPI d’affichage fréquemment modifiés plusieurs fois pendant la durée de vie d’un processus d’application.</span><span class="sxs-lookup"><span data-stu-id="09d2d-115">This assumption no longer holds true, with display DPIs commonly changing several times throughout an application process's lifetime.</span></span> <span data-ttu-id="09d2d-116">Voici quelques scénarios courants dans lesquels le facteur d’échelle d’affichage/DPI change :</span><span class="sxs-lookup"><span data-stu-id="09d2d-116">Some common scenarios where the display scale factor/DPI changes are:</span></span>

-   <span data-ttu-id="09d2d-117">Configurations à plusieurs écrans où chaque affichage a un facteur d’échelle différent et l’application est déplacée d’un affichage à un autre (par exemple, 4 Ko et un affichage de 1080p)</span><span class="sxs-lookup"><span data-stu-id="09d2d-117">Multiple-monitor setups where each display has a different scale factor and the application is moved from one display to another (such as a 4K and a 1080p display)</span></span>
-   <span data-ttu-id="09d2d-118">Ancrage et déconnexion d’un ordinateur portable haute résolution avec un affichage externe à basse résolution (ou vice versa)</span><span class="sxs-lookup"><span data-stu-id="09d2d-118">Docking and undocking a high DPI laptop with a low-DPI external display (or vice versa)</span></span>
-   <span data-ttu-id="09d2d-119">Connexion via Bureau à distance d’un ordinateur portable/tablette haute résolution à un appareil basse résolution (ou vice versa)</span><span class="sxs-lookup"><span data-stu-id="09d2d-119">Connecting via Remote Desktop from a high DPI laptop/tablet to a low-DPI device (or vice versa)</span></span>
-   <span data-ttu-id="09d2d-120">Modification des paramètres d’affichage-facteur d’échelle pendant l’exécution des applications</span><span class="sxs-lookup"><span data-stu-id="09d2d-120">Making a display-scale-factor settings change while applications are running</span></span>

<span data-ttu-id="09d2d-121">Dans ces scénarios, les applications UWP se redessinent automatiquement pour la nouvelle résolution.</span><span class="sxs-lookup"><span data-stu-id="09d2d-121">In these scenarios, UWP applications redraw themselves for the new DPI automatically.</span></span> <span data-ttu-id="09d2d-122">Par défaut, et sans travail supplémentaire des développeurs, les applications de bureau ne le font pas.</span><span class="sxs-lookup"><span data-stu-id="09d2d-122">By default, and without additional developer work, desktop applications do not.</span></span> <span data-ttu-id="09d2d-123">Les applications de bureau qui n’effectuent pas ce travail supplémentaire pour répondre aux modifications PPP peuvent apparaître floues ou incorrectement dimensionnées pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="09d2d-123">Desktop applications that don't do this extra work to respond to DPI changes may appear blurry or incorrectly-sized to the user.</span></span>

## <a name="dpi-awareness-mode"></a><span data-ttu-id="09d2d-124">Mode de reconnaissance DPI</span><span class="sxs-lookup"><span data-stu-id="09d2d-124">DPI Awareness Mode</span></span>

<span data-ttu-id="09d2d-125">Les applications de bureau doivent indiquer à Windows si elles prennent en charge la mise à l’échelle DPI.</span><span class="sxs-lookup"><span data-stu-id="09d2d-125">Desktop applications must tell Windows if they support DPI scaling.</span></span> <span data-ttu-id="09d2d-126">Par défaut, le système considère que les applications de bureau ne prennent pas en charge PPP et étire leurs fenêtres.</span><span class="sxs-lookup"><span data-stu-id="09d2d-126">By default, the system considers desktop applications DPI unaware and bitmap-stretches their windows.</span></span> <span data-ttu-id="09d2d-127">En définissant l’un des modes de reconnaissance PPP disponibles suivants, les applications peuvent explicitement indiquer à Windows comment elles souhaitent gérer la mise à l’échelle DPI :</span><span class="sxs-lookup"><span data-stu-id="09d2d-127">By setting one of the following available DPI awareness modes, applications can explicitly tell Windows how they wish to handle DPI scaling:</span></span>

### <a name="dpi-unaware"></a><span data-ttu-id="09d2d-128">Prise en charge de DPI</span><span class="sxs-lookup"><span data-stu-id="09d2d-128">DPI Unaware</span></span>

<span data-ttu-id="09d2d-129">Les applications sans prise en charge DPI sont rendues à une valeur DPI fixe de 96 (100%).</span><span class="sxs-lookup"><span data-stu-id="09d2d-129">DPI unaware applications render at a fixed DPI value of 96 (100%).</span></span> <span data-ttu-id="09d2d-130">Chaque fois que ces applications sont exécutées sur un écran avec une échelle d’affichage supérieure à 96 ppp, Windows étend la bitmap de l’application à la taille physique attendue.</span><span class="sxs-lookup"><span data-stu-id="09d2d-130">Whenever these applications are run on a screen with a display scale greater than 96 DPI, Windows will stretch the application bitmap to the expected physical size.</span></span> <span data-ttu-id="09d2d-131">Cela entraîne l’affichage de l’application floue.</span><span class="sxs-lookup"><span data-stu-id="09d2d-131">This results in the application appearing blurry.</span></span>

### <a name="system-dpi-awareness"></a><span data-ttu-id="09d2d-132">Reconnaissance du système DPI</span><span class="sxs-lookup"><span data-stu-id="09d2d-132">System DPI Awareness</span></span>

<span data-ttu-id="09d2d-133">Les applications de bureau qui prennent en charge le système DPI reçoivent généralement les PPP de l’analyse connectée principale au moment de la connexion de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="09d2d-133">Desktop applications that are system DPI aware typically receive the DPI of the primary connected monitor as of the time of user sign-in.</span></span> <span data-ttu-id="09d2d-134">Pendant l’initialisation, ils présentent leur interface utilisateur de manière appropriée (dimensionnement des contrôles, choix de la taille des polices, chargement des ressources, etc.) à l’aide de cette valeur DPI système.</span><span class="sxs-lookup"><span data-stu-id="09d2d-134">During initialization, they lay out their UI appropriately (sizing controls, choosing font sizes, loading assets, etc.) using that System DPI value.</span></span> <span data-ttu-id="09d2d-135">Par conséquent, les applications prenant en charge DPI système ne sont pas mises à l’échelle DPI (bitmap étirée) par Windows sur affiche le rendu à cette seule résolution.</span><span class="sxs-lookup"><span data-stu-id="09d2d-135">As such, System DPI-aware applications are not DPI scaled (bitmap stretched) by Windows on displays rendering at that single DPI.</span></span> <span data-ttu-id="09d2d-136">Lorsque l’application est déplacée vers un affichage avec un facteur d’échelle différent, ou si le facteur d’échelle de l’affichage change, Windows met à l’échelle les fenêtres de l’application, ce qui les rend floues.</span><span class="sxs-lookup"><span data-stu-id="09d2d-136">When the application is moved to a display with a different scale factor, or if the display scale factor otherwise changes, Windows will bitmap scale the application's windows, making them appear blurry.</span></span> <span data-ttu-id="09d2d-137">En fait, les applications de bureau prenant en charge le système DPI ne s’affichent qu’à un seul facteur d’échelle d’affichage, ce qui devient flou à chaque modification de la résolution.</span><span class="sxs-lookup"><span data-stu-id="09d2d-137">Effectively, System DPI-aware desktop applications only render crisply at a single display scale factor, becoming blurry whenever the DPI changes.</span></span>

### <a name="per-monitor-and-per-monitor-v2-dpi-awareness"></a><span data-ttu-id="09d2d-138">Détection des PPP Per-Monitor et Per-Monitor (v2)</span><span class="sxs-lookup"><span data-stu-id="09d2d-138">Per-Monitor and Per-Monitor (V2) DPI Awareness</span></span>

<span data-ttu-id="09d2d-139">Il est recommandé que les applications de bureau soient mises à jour pour utiliser le mode de reconnaissance DPI par moniteur, ce qui leur permet d’effectuer un rendu correct immédiatement à chaque modification de la résolution.</span><span class="sxs-lookup"><span data-stu-id="09d2d-139">It is recommended that desktop applications be updated to use per-monitor DPI awareness mode, allowing them to immediately render correctly whenever the DPI changes.</span></span> <span data-ttu-id="09d2d-140">Quand une application signale à Windows qu’elle souhaite s’exécuter dans ce mode, Windows n’étire pas l’application en mode Bitmap lorsque la valeur PPP change, en envoyant [WM \_ DPICHANGED](wm-dpichanged.md) à la fenêtre d’application.</span><span class="sxs-lookup"><span data-stu-id="09d2d-140">When an application reports to Windows that it wants to run in this mode, Windows will not bitmap stretch the application when the DPI changes, instead sending [WM\_DPICHANGED](wm-dpichanged.md) to the application window.</span></span> <span data-ttu-id="09d2d-141">Il incombe ensuite à l’application de gérer le redimensionnement proprement dit pour la nouvelle résolution PPP.</span><span class="sxs-lookup"><span data-stu-id="09d2d-141">It is then the complete responsibility of the application to handle resizing itself for the new DPI.</span></span> <span data-ttu-id="09d2d-142">La plupart des infrastructures d’interface utilisateur utilisées par les applications de bureau (les contrôles communs Windows (ComCtl32), Windows Forms, Windows Presentation Framework, etc.) ne prennent pas en charge la mise à l’échelle PPP automatique, ce qui oblige les développeurs à redimensionner et à repositionner le contenu de leurs fenêtres elles-mêmes.</span><span class="sxs-lookup"><span data-stu-id="09d2d-142">Most UI frameworks used by desktop applications (Windows common controls (comctl32), Windows Forms, Windows Presentation Framework, etc.) do not support automatic DPI scaling, requiring developers to resize and reposition the contents of their windows themselves.</span></span>

<span data-ttu-id="09d2d-143">Il existe deux versions de Per-Monitor savoir qu’une application peut s’inscrire elle-même en tant que version 1 et version 2 (PMv2).</span><span class="sxs-lookup"><span data-stu-id="09d2d-143">There are two versions of Per-Monitor awareness that an application can register itself as: version 1 and version 2 (PMv2).</span></span> <span data-ttu-id="09d2d-144">L’inscription d’un processus comme s’exécutant en mode de sensibilisation PMv2 génère les résultats suivants :</span><span class="sxs-lookup"><span data-stu-id="09d2d-144">Registering a process as running in PMv2 awareness mode results in:</span></span>

1.  <span data-ttu-id="09d2d-145">L’application qui est avertie lorsque la DPI change (à la fois les HWND de niveau supérieur et enfant)</span><span class="sxs-lookup"><span data-stu-id="09d2d-145">The application being notified when the DPI changes (both the top-level and child HWNDs)</span></span>
2.  <span data-ttu-id="09d2d-146">L’application visualisant les pixels bruts de chaque affichage</span><span class="sxs-lookup"><span data-stu-id="09d2d-146">The application seeing the raw pixels of each display</span></span>
3.  <span data-ttu-id="09d2d-147">L’application n’est jamais bitmap mise à l’échelle par Windows</span><span class="sxs-lookup"><span data-stu-id="09d2d-147">The application never being bitmap scaled by Windows</span></span>
4.  <span data-ttu-id="09d2d-148">Zone non cliente automatique (titre de fenêtre, barres de défilement, etc.) Mise à l’échelle DPI par Windows</span><span class="sxs-lookup"><span data-stu-id="09d2d-148">Automatic non-client area (window caption, scroll bars, etc.) DPI scaling by Windows</span></span>
5.  <span data-ttu-id="09d2d-149">Dialogues Win32 (à partir de [createDialog](/windows/desktop/api/winuser/nf-winuser-createdialogw)) automatiquement PPP mis à l’échelle par Windows</span><span class="sxs-lookup"><span data-stu-id="09d2d-149">Win32 dialogs (from [CreateDialog](/windows/desktop/api/winuser/nf-winuser-createdialogw)) automatically DPI scaled by Windows</span></span>
6.  <span data-ttu-id="09d2d-150">Ressources bitmap dessinées par thème dans les contrôles communs (cases à cocher, arrière-plans de bouton, etc.) qui s’affichent automatiquement au facteur d’échelle PPP approprié</span><span class="sxs-lookup"><span data-stu-id="09d2d-150">Theme-drawn bitmap assets in common controls (checkboxes, button backgrounds, etc.) being automatically rendered at the appropriate DPI scale factor</span></span>

<span data-ttu-id="09d2d-151">En cas d’exécution en mode de sensibilisation à Per-Monitor v2, les applications sont averties lorsque leur PPP a changé.</span><span class="sxs-lookup"><span data-stu-id="09d2d-151">When running in Per-Monitor v2 Awareness mode, applications are notified when their DPI has changed.</span></span> <span data-ttu-id="09d2d-152">Si une application ne se redimensionne pas pour la nouvelle résolution, l’interface utilisateur de l’application apparaîtra trop petite ou trop grande (en fonction de la différence dans les valeurs PPP précédentes et nouvelles).</span><span class="sxs-lookup"><span data-stu-id="09d2d-152">If an application does not resize itself for the new DPI, the application UI will appear too small or too large (depending on the difference in the previous and new DPI values).</span></span>

> [!Note]  
> <span data-ttu-id="09d2d-153">La sensibilisation à Per-Monitor v1 (PMv1) est très limitée.</span><span class="sxs-lookup"><span data-stu-id="09d2d-153">Per-Monitor V1 (PMv1) awareness is very limited.</span></span> <span data-ttu-id="09d2d-154">Il est recommandé que les applications utilisent PMv2.</span><span class="sxs-lookup"><span data-stu-id="09d2d-154">It is recommended that applications use PMv2.</span></span>

<span data-ttu-id="09d2d-155">Le tableau suivant montre comment les applications s’affichent sous différents scénarios :</span><span class="sxs-lookup"><span data-stu-id="09d2d-155">The following table shows how applications will render under different scenarios:</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="09d2d-156">Mode de reconnaissance DPI</span><span class="sxs-lookup"><span data-stu-id="09d2d-156">DPI Awareness Mode</span></span></th>
<th><span data-ttu-id="09d2d-157">Version de Windows introduite</span><span class="sxs-lookup"><span data-stu-id="09d2d-157">Windows Version Introduced</span></span></th>
<th><span data-ttu-id="09d2d-158">Affichage de l’application en PPP</span><span class="sxs-lookup"><span data-stu-id="09d2d-158">Application's view of DPI</span></span></th>
<th><span data-ttu-id="09d2d-159">Comportement sur la modification PPP</span><span class="sxs-lookup"><span data-stu-id="09d2d-159">Behavior on DPI change</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="09d2d-160">Ignore</span><span class="sxs-lookup"><span data-stu-id="09d2d-160">Unaware</span></span></td>
<td><span data-ttu-id="09d2d-161">N/A</span><span class="sxs-lookup"><span data-stu-id="09d2d-161">N/A</span></span></td>
<td><span data-ttu-id="09d2d-162">Tous les affichages sont de 96 ppp</span><span class="sxs-lookup"><span data-stu-id="09d2d-162">All displays are 96 DPI</span></span></td>
<td><span data-ttu-id="09d2d-163">Étirement de bitmap (flou)</span><span class="sxs-lookup"><span data-stu-id="09d2d-163">Bitmap-stretching (blurry)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="09d2d-164">Système</span><span class="sxs-lookup"><span data-stu-id="09d2d-164">System</span></span></td>
<td><span data-ttu-id="09d2d-165">Vista</span><span class="sxs-lookup"><span data-stu-id="09d2d-165">Vista</span></span></td>
<td><span data-ttu-id="09d2d-166">Tous les affichages ont le même PPP (la résolution PPP de l’affichage principal au moment du démarrage de la session de l’utilisateur actuel)</span><span class="sxs-lookup"><span data-stu-id="09d2d-166">All displays have the same DPI (the DPI of the primary display at the time the current user session was started)</span></span></td>
<td><span data-ttu-id="09d2d-167">Étirement de bitmap (flou)</span><span class="sxs-lookup"><span data-stu-id="09d2d-167">Bitmap-stretching (blurry)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="09d2d-168">Per-Monitor</span><span class="sxs-lookup"><span data-stu-id="09d2d-168">Per-Monitor</span></span></td>
<td><span data-ttu-id="09d2d-169">8.1</span><span class="sxs-lookup"><span data-stu-id="09d2d-169">8.1</span></span></td>
<td><span data-ttu-id="09d2d-170">PPP de l’affichage sur lequel la fenêtre d’application se trouve principalement</span><span class="sxs-lookup"><span data-stu-id="09d2d-170">The DPI of the display that the application window is primarily located on</span></span></td>
<td><ul>
<li><span data-ttu-id="09d2d-171">Le HWND de niveau supérieur est informé de la modification PPP</span><span class="sxs-lookup"><span data-stu-id="09d2d-171">Top-level HWND is notified of DPI change</span></span></li>
<li><span data-ttu-id="09d2d-172">Aucune mise à l’échelle DPI de tout élément d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="09d2d-172">No DPI scaling of any UI elements.</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="09d2d-173">Per-Monitor V2</span><span class="sxs-lookup"><span data-stu-id="09d2d-173">Per-Monitor V2</span></span></td>
<td><span data-ttu-id="09d2d-174">Windows 10 Creators Update (1703)</span><span class="sxs-lookup"><span data-stu-id="09d2d-174">Windows 10 Creators Update (1703)</span></span></td>
<td><span data-ttu-id="09d2d-175">PPP de l’affichage sur lequel la fenêtre d’application se trouve principalement</span><span class="sxs-lookup"><span data-stu-id="09d2d-175">The DPI of the display that the application window is primarily located on</span></span></td>
<td><ul>
<li><span data-ttu-id="09d2d-176">Les HWND de niveau supérieur <span class="underline">et</span> enfant sont avertis de la modification PPP</span><span class="sxs-lookup"><span data-stu-id="09d2d-176">Top-level <span class="underline">and</span> child HWNDs are notified of DPI change</span></span></li>
</ul>
<br/> <span data-ttu-id="09d2d-177"><span class="underline">Mise à l’échelle DPI automatique de :</span>
</span><span class="sxs-lookup"><span data-stu-id="09d2d-177"><span class="underline">Automatic DPI scaling of:</span>
</span></span><ul>
<li><span data-ttu-id="09d2d-178">Zone non cliente</span><span class="sxs-lookup"><span data-stu-id="09d2d-178">Non-client area</span></span></li>
<li><span data-ttu-id="09d2d-179">Bitmaps dessinées par thème dans les contrôles communs (ComCtl32 V6)</span><span class="sxs-lookup"><span data-stu-id="09d2d-179">Theme-drawn bitmaps in common controls (comctl32 V6)</span></span></li>
<li><span data-ttu-id="09d2d-180">Boîtes de dialogue (<a href="/windows/desktop/api/winuser/nf-winuser-createdialogw">createDialog</a>)</span><span class="sxs-lookup"><span data-stu-id="09d2d-180">Dialogs (<a href="/windows/desktop/api/winuser/nf-winuser-createdialogw">CreateDialog</a>)</span></span></li>
</ul>
<br/></td>
</tr>
</tbody>
</table>

### <a name="per-monitor-v1-dpi-awareness"></a><span data-ttu-id="09d2d-181">Reconnaissance par analyse (v1) ppp</span><span class="sxs-lookup"><span data-stu-id="09d2d-181">Per Monitor (V1) DPI Awareness</span></span>

<span data-ttu-id="09d2d-182">Per-Monitor v1 (PMv1 v1 Awareness mode Awareness) a été introduit avec Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="09d2d-182">Per-Monitor V1 DPI awareness mode (PMv1) was introduced with Windows 8.1.</span></span> <span data-ttu-id="09d2d-183">Ce mode de reconnaissance des PPP est très limité et offre uniquement les fonctionnalités listées ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="09d2d-183">This DPI awareness mode is very limited and only offers the functionality listed below.</span></span> <span data-ttu-id="09d2d-184">Il est recommandé que les applications de bureau utilisent le mode de sensibilisation Per-Monitor v2, pris en charge sur Windows 10 1703 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="09d2d-184">It is recommended that desktop applications use Per-Monitor v2 awareness mode, supported on Windows 10 1703 or above.</span></span>

<span data-ttu-id="09d2d-185">La prise en charge initiale de la reconnaissance par moniteur ne proposait que les applications suivantes :</span><span class="sxs-lookup"><span data-stu-id="09d2d-185">The initial support for per-monitor awareness only offered applications the following:</span></span>

1.  <span data-ttu-id="09d2d-186">Les HWND de niveau supérieur sont avertis d’une modification PPP et ont fourni une nouvelle taille suggérée</span><span class="sxs-lookup"><span data-stu-id="09d2d-186">Top-level HWNDs are notified of a DPI change and provided a new suggested size</span></span>
2.  <span data-ttu-id="09d2d-187">Windows n’étire pas l’interface utilisateur de l’application</span><span class="sxs-lookup"><span data-stu-id="09d2d-187">Windows will not bitmap stretch the application UI</span></span>
3.  <span data-ttu-id="09d2d-188">L’application voit tous les affichages en pixels physiques (voir virtualisation)</span><span class="sxs-lookup"><span data-stu-id="09d2d-188">The application sees all displays in physical pixels (see virtualization)</span></span>

<span data-ttu-id="09d2d-189">Sur Windows 10 1607 ou version ultérieure, les applications PMv1 peuvent également appeler [EnableNonClientDpiScaling](/windows/desktop/api/winuser/nf-winuser-enablenonclientdpiscaling) pendant \_ le NCCREATE WM pour demander que Windows fasse correctement évoluer la zone non cliente de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="09d2d-189">On Windows 10 1607 or above, PMv1 applications may also call [EnableNonClientDpiScaling](/windows/desktop/api/winuser/nf-winuser-enablenonclientdpiscaling) during WM\_NCCREATE to request that Windows correctly scale the window's non-client area.</span></span>

## <a name="per-monitor-dpi-scaling-support-by-ui-framework--technology"></a><span data-ttu-id="09d2d-190">Prise en charge de la mise à l’échelle DPI par moniteur par infrastructure/infrastructure d’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="09d2d-190">Per Monitor DPI Scaling Support by UI Framework / Technology</span></span>

<span data-ttu-id="09d2d-191">Le tableau ci-dessous montre le niveau de prise en charge de la prise en charge DPI par moniteur offert par plusieurs infrastructures d’interface utilisateur Windows à partir de Windows 10 1703 :</span><span class="sxs-lookup"><span data-stu-id="09d2d-191">The table below shows the level of per-monitor DPI awareness support offered by various Windows UI frameworks as of Windows 10 1703:</span></span>

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
<th><span data-ttu-id="09d2d-192">Infrastructure/technologie</span><span class="sxs-lookup"><span data-stu-id="09d2d-192">Framework / Technology</span></span></th>
<th><span data-ttu-id="09d2d-193">Support</span><span class="sxs-lookup"><span data-stu-id="09d2d-193">Support</span></span></th>
<th><span data-ttu-id="09d2d-194">Version du SE</span><span class="sxs-lookup"><span data-stu-id="09d2d-194">OS Version</span></span></th>
<th><span data-ttu-id="09d2d-195">Mise à l’échelle DPI gérée par</span><span class="sxs-lookup"><span data-stu-id="09d2d-195">DPI Scaling handled by</span></span></th>
<th><span data-ttu-id="09d2d-196">En savoir plus</span><span class="sxs-lookup"><span data-stu-id="09d2d-196">Further Reading</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="09d2d-197">Plateforme Windows universelle (UWP)</span><span class="sxs-lookup"><span data-stu-id="09d2d-197">Universal Windows Platform (UWP)</span></span></td>
<td><span data-ttu-id="09d2d-198">Complète</span><span class="sxs-lookup"><span data-stu-id="09d2d-198">Full</span></span></td>
<td><span data-ttu-id="09d2d-199">1607</span><span class="sxs-lookup"><span data-stu-id="09d2d-199">1607</span></span></td>
<td><span data-ttu-id="09d2d-200">Infrastructure d’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="09d2d-200">UI framework</span></span></td>
<td><span data-ttu-id="09d2d-201"><a href="/windows/uwp/get-started/whats-a-uwp">Plateforme Windows universelle (UWP)</a></span><span class="sxs-lookup"><span data-stu-id="09d2d-201"><a href="/windows/uwp/get-started/whats-a-uwp">Universal Windows Platform (UWP)</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="09d2d-202">Commandes Win32/Common Controls (comctl32.dll) brutes</span><span class="sxs-lookup"><span data-stu-id="09d2d-202">Raw Win32/Common Controls V6 (comctl32.dll)</span></span></td>
<td><ul>
<li><span data-ttu-id="09d2d-203">Messages de notification de changement DPI envoyés à tous les HWND</span><span class="sxs-lookup"><span data-stu-id="09d2d-203">DPI change notification messages sent to all HWNDs</span></span></li>
<li><span data-ttu-id="09d2d-204">Les ressources dessinées par thème sont rendues correctement dans les contrôles communs</span><span class="sxs-lookup"><span data-stu-id="09d2d-204">Theme-drawn assets render correctly in common controls</span></span></li>
<li><span data-ttu-id="09d2d-205">Mise à l’échelle DPI automatique pour les boîtes de dialogue</span><span class="sxs-lookup"><span data-stu-id="09d2d-205">Automatic DPI scaling for dialogs</span></span></li>
</ul></td>
<td><span data-ttu-id="09d2d-206">1703</span><span class="sxs-lookup"><span data-stu-id="09d2d-206">1703</span></span></td>
<td><span data-ttu-id="09d2d-207">Application</span><span class="sxs-lookup"><span data-stu-id="09d2d-207">Application</span></span></td>
<td><span data-ttu-id="09d2d-208"><a href="https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DPIAwarenessPerWindow">Exemple GitHub</a></span><span class="sxs-lookup"><span data-stu-id="09d2d-208"><a href="https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DPIAwarenessPerWindow">GitHub Sample</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="09d2d-209">Windows Forms</span><span class="sxs-lookup"><span data-stu-id="09d2d-209">Windows Forms</span></span></td>
<td><span data-ttu-id="09d2d-210">Mise à l’échelle DPI automatique par moniteur limitée pour certains contrôles</span><span class="sxs-lookup"><span data-stu-id="09d2d-210">Limited automatic per-monitor DPI scaling for some controls</span></span></td>
<td><span data-ttu-id="09d2d-211">1703</span><span class="sxs-lookup"><span data-stu-id="09d2d-211">1703</span></span></td>
<td><span data-ttu-id="09d2d-212">Infrastructure d’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="09d2d-212">UI framework</span></span></td>
<td><span data-ttu-id="09d2d-213"><a href="/dotnet/framework/winforms/high-dpi-support-in-windows-forms">Prise en charge des résolutions élevées en Windows Forms</a></span><span class="sxs-lookup"><span data-stu-id="09d2d-213"><a href="/dotnet/framework/winforms/high-dpi-support-in-windows-forms">High DPI Support in Windows Forms</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="09d2d-214">Windows Presentation Framework (WPF)</span><span class="sxs-lookup"><span data-stu-id="09d2d-214">Windows Presentation Framework (WPF)</span></span></td>
<td><span data-ttu-id="09d2d-215">Les applications WPF natives prennent en charge la résolution de WPF hébergée dans d’autres infrastructures et d’autres infrastructures hébergées dans WPF ne sont pas automatiquement mises à l’échelle</span><span class="sxs-lookup"><span data-stu-id="09d2d-215">Native WPF applications will DPI scale WPF hosted in other frameworks and other frameworks hosted in WPF do not automatically scale</span></span></td>
<td><span data-ttu-id="09d2d-216">1607</span><span class="sxs-lookup"><span data-stu-id="09d2d-216">1607</span></span></td>
<td><span data-ttu-id="09d2d-217">Infrastructure d’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="09d2d-217">UI framework</span></span></td>
<td><span data-ttu-id="09d2d-218"><a href="https://github.com/Microsoft/WPF-Samples/tree/master/PerMonitorDPI">Exemple GitHub</a></span><span class="sxs-lookup"><span data-stu-id="09d2d-218"><a href="https://github.com/Microsoft/WPF-Samples/tree/master/PerMonitorDPI">GitHub Sample</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="09d2d-219">GDI</span><span class="sxs-lookup"><span data-stu-id="09d2d-219">GDI</span></span></td>
<td><span data-ttu-id="09d2d-220">None</span><span class="sxs-lookup"><span data-stu-id="09d2d-220">None</span></span></td>
<td><span data-ttu-id="09d2d-221">N/A</span><span class="sxs-lookup"><span data-stu-id="09d2d-221">N/A</span></span></td>
<td><span data-ttu-id="09d2d-222">Application</span><span class="sxs-lookup"><span data-stu-id="09d2d-222">Application</span></span></td>
<td><span data-ttu-id="09d2d-223">Voir <a href="https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/">mise à l’échelle GDI haute résolution</a></span><span class="sxs-lookup"><span data-stu-id="09d2d-223">See <a href="https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/">GDI High-DPI Scaling</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="09d2d-224">GDI+</span><span class="sxs-lookup"><span data-stu-id="09d2d-224">GDI+</span></span></td>
<td><span data-ttu-id="09d2d-225">None</span><span class="sxs-lookup"><span data-stu-id="09d2d-225">None</span></span></td>
<td><span data-ttu-id="09d2d-226">N/A</span><span class="sxs-lookup"><span data-stu-id="09d2d-226">N/A</span></span></td>
<td><span data-ttu-id="09d2d-227">Application</span><span class="sxs-lookup"><span data-stu-id="09d2d-227">Application</span></span></td>
<td><span data-ttu-id="09d2d-228">Voir <a href="https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/">mise à l’échelle GDI haute résolution</a></span><span class="sxs-lookup"><span data-stu-id="09d2d-228">See <a href="https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/">GDI High-DPI Scaling</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="09d2d-229">MFC</span><span class="sxs-lookup"><span data-stu-id="09d2d-229">MFC</span></span></td>
<td><span data-ttu-id="09d2d-230">None</span><span class="sxs-lookup"><span data-stu-id="09d2d-230">None</span></span></td>
<td><span data-ttu-id="09d2d-231">N/A</span><span class="sxs-lookup"><span data-stu-id="09d2d-231">N/A</span></span></td>
<td><span data-ttu-id="09d2d-232">Application</span><span class="sxs-lookup"><span data-stu-id="09d2d-232">Application</span></span></td>
<td><span data-ttu-id="09d2d-233">N/A</span><span class="sxs-lookup"><span data-stu-id="09d2d-233">N/A</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="updating-existing-applications"></a><span data-ttu-id="09d2d-234">Mise à jour des applications existantes</span><span class="sxs-lookup"><span data-stu-id="09d2d-234">Updating Existing Applications</span></span>

<span data-ttu-id="09d2d-235">Pour mettre à jour une application de bureau existante afin de gérer correctement la mise à l’échelle DPI, elle doit être mise à jour de telle sorte qu’au minimum, les parties importantes de l’interface utilisateur soient mises à jour pour répondre aux modifications PPP.</span><span class="sxs-lookup"><span data-stu-id="09d2d-235">In order to update an existing desktop application to handle DPI scaling properly, it needs to be updated such that, at a minimum, the important parts of its UI are updated to respond to DPI changes.</span></span>

<span data-ttu-id="09d2d-236">La plupart des applications de bureau s’exécutent en mode de reconnaissance DPI système.</span><span class="sxs-lookup"><span data-stu-id="09d2d-236">Most desktop applications run under system DPI awareness mode.</span></span> <span data-ttu-id="09d2d-237">Les applications prenant en charge DPI système sont généralement mises à l’échelle en fonction de la résolution de l’affichage principal (l’affichage dans lequel se trouvait la barre d’état système au moment du démarrage de la session Windows).</span><span class="sxs-lookup"><span data-stu-id="09d2d-237">System-DPI-aware applications typically scale to the DPI of the primary display (the display that the system tray was located on at the time the Windows session was started).</span></span> <span data-ttu-id="09d2d-238">Lorsque les PPP changent, Windows étire la bitmap de l’interface utilisateur de ces applications, ce qui entraîne souvent un flou.</span><span class="sxs-lookup"><span data-stu-id="09d2d-238">When the DPI changes, Windows will bitmap stretch the UI of these applications, which often results in them being blurry.</span></span> <span data-ttu-id="09d2d-239">Lors de la mise à jour d’une application compatible DPI du système pour qu’elle prenne en charge la résolution par moniteur, le code qui gère la disposition de l’interface utilisateur doit être mis à jour de manière à ce qu’il soit exécuté non seulement pendant l’initialisation de l’application, mais aussi chaque fois qu’une notification de modification DPI ([WM \_ DPICHANGED](wm-dpichanged.md) dans le cas de Win32) est reçue.</span><span class="sxs-lookup"><span data-stu-id="09d2d-239">When updating a System DPI-aware application to become per-monitor-DPI aware, the code which handles UI layout needs to be updated such that it is performed not only during application initialization, but also whenever a DPI change notification ([WM\_DPICHANGED](wm-dpichanged.md) in the case of Win32) is received.</span></span> <span data-ttu-id="09d2d-240">Cela implique généralement de revisiter les hypothèses du code dont l’interface utilisateur ne doit être mise à l’échelle qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="09d2d-240">This typically involves revisiting any assumptions in the code that the UI only needs to be scaled once.</span></span>

<span data-ttu-id="09d2d-241">En outre, dans le cas de la programmation Win32, de nombreuses API Win32 n’ont pas de résolution ou de contexte d’affichage, de sorte qu’elles ne retournent que des valeurs par rapport à la DPI système.</span><span class="sxs-lookup"><span data-stu-id="09d2d-241">Also, in the case of Win32 programming, many Win32 APIs do not have any DPI or display context so they will only return values relative to the System DPI.</span></span> <span data-ttu-id="09d2d-242">Il peut être utile de parcourir votre code pour rechercher certaines de ces API et de les remplacer par des variantes compatibles PPP.</span><span class="sxs-lookup"><span data-stu-id="09d2d-242">It can be useful to grep through your code to look for some of these APIs and replace them with DPI-aware variants.</span></span> <span data-ttu-id="09d2d-243">Voici quelques-unes des API courantes qui ont des variantes prenant en charge la résolution :</span><span class="sxs-lookup"><span data-stu-id="09d2d-243">Some of the common APIs that have DPI-aware variants are:</span></span>



| <span data-ttu-id="09d2d-244">Version à PPP unique</span><span class="sxs-lookup"><span data-stu-id="09d2d-244">Single DPI version</span></span>   | <span data-ttu-id="09d2d-245">Version de Per-Monitor</span><span class="sxs-lookup"><span data-stu-id="09d2d-245">Per-Monitor version</span></span>        |
|----------------------|----------------------------|
| <span data-ttu-id="09d2d-246">GetSystemMetrics</span><span class="sxs-lookup"><span data-stu-id="09d2d-246">GetSystemMetrics</span></span>     | <span data-ttu-id="09d2d-247">GetSystemMetricsForDpi</span><span class="sxs-lookup"><span data-stu-id="09d2d-247">GetSystemMetricsForDpi</span></span>     |
| <span data-ttu-id="09d2d-248">AdjustWindowRectEx</span><span class="sxs-lookup"><span data-stu-id="09d2d-248">AdjustWindowRectEx</span></span>   | <span data-ttu-id="09d2d-249">AdjustWindowRectExForDpi</span><span class="sxs-lookup"><span data-stu-id="09d2d-249">AdjustWindowRectExForDpi</span></span>   |
| <span data-ttu-id="09d2d-250">SystemParametersInfo</span><span class="sxs-lookup"><span data-stu-id="09d2d-250">SystemParametersInfo</span></span> | <span data-ttu-id="09d2d-251">SystemParametersInfoForDpi</span><span class="sxs-lookup"><span data-stu-id="09d2d-251">SystemParametersInfoForDpi</span></span> |
| <span data-ttu-id="09d2d-252">GetDpiForMonitor</span><span class="sxs-lookup"><span data-stu-id="09d2d-252">GetDpiForMonitor</span></span>     | <span data-ttu-id="09d2d-253">GetDpiForWindow</span><span class="sxs-lookup"><span data-stu-id="09d2d-253">GetDpiForWindow</span></span>            |



 

<span data-ttu-id="09d2d-254">Il est également judicieux de rechercher les tailles codées en dur dans votre code base qui supposent une résolution constante, en les remplaçant par du code qui compte correctement la mise à l’échelle PPP.</span><span class="sxs-lookup"><span data-stu-id="09d2d-254">It is also a good idea to search for hard-coded sizes in your codebase that assume a constant DPI, replacing them with code that correctly accounts for DPI scaling.</span></span> <span data-ttu-id="09d2d-255">Voici un exemple qui incorpore toutes ces suggestions :</span><span class="sxs-lookup"><span data-stu-id="09d2d-255">Below is an example that incorporates all of these suggestions:</span></span>

### <a name="example"></a><span data-ttu-id="09d2d-256">Exemple :</span><span class="sxs-lookup"><span data-stu-id="09d2d-256">Example:</span></span>

<span data-ttu-id="09d2d-257">L’exemple ci-dessous montre un cas simplifié en cas de création d’un HWND enfant.</span><span class="sxs-lookup"><span data-stu-id="09d2d-257">The example below shows a simplified Win32 case of creating a child HWND.</span></span> <span data-ttu-id="09d2d-258">L’appel à CreateWindow suppose que l’application s’exécute à 96 ppp, et que la taille et la position du bouton ne sont pas correctes à un niveau dpi supérieur :</span><span class="sxs-lookup"><span data-stu-id="09d2d-258">The call to CreateWindow assumes that the application is running at 96 DPI, and neither the button's size nor position will be correct at higher DPIs:</span></span>


```
case WM_CREATE: 
{ 
    // Add a button 
    HWND hWndChild = CreateWindow(L"BUTTON", L"Click Me",  
        WS_CHILD|WS_VISIBLE|BS_PUSHBUTTON,  
        50,  
        50,  
        100,  
        50,  
        hWnd, (HMENU)NULL, NULL, NULL); 
} 
```



<span data-ttu-id="09d2d-259">Le code mis à jour ci-dessous montre les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="09d2d-259">The updated code below shows:</span></span>

1.  <span data-ttu-id="09d2d-260">Code PPP de création de fenêtres mettant à l’échelle la position et la taille du HWND enfant pour la résolution de sa fenêtre parente</span><span class="sxs-lookup"><span data-stu-id="09d2d-260">The window-creation code DPI scaling the position and size of the child HWND for the DPI of its parent window</span></span>
2.  <span data-ttu-id="09d2d-261">Réponse aux modifications PPP par repositionnement et redimensionnement du HWND enfant</span><span class="sxs-lookup"><span data-stu-id="09d2d-261">Responding to DPI change by repositioning and resizing the child HWND</span></span>
3.  <span data-ttu-id="09d2d-262">Tailles codées en dur supprimées et remplacées par du code qui répond aux modifications PPP</span><span class="sxs-lookup"><span data-stu-id="09d2d-262">Hard-coded sizes removed and replaced with code that responds to DPI changes</span></span>


```
#define INITIALX_96DPI 50 
#define INITIALY_96DPI 50 
#define INITIALWIDTH_96DPI 100 
#define INITIALHEIGHT_96DPI 50 
 
 
// DPI scale the position and size of the button control 
void UpdateButtonLayoutForDpi(HWND hWnd) 
{ 
    int iDpi = GetDpiForWindow(hWnd); 
    int dpiScaledX = MulDiv(INITIALX_96DPI, iDpi, 96); 
    int dpiScaledY = MulDiv(INITIALY_96DPI, iDpi, 96); 
    int dpiScaledWidth = MulDiv(INITIALWIDTH_96DPI, iDpi, 96); 
    int dpiScaledHeight = MulDiv(INITIALHEIGHT_96DPI, iDpi, 96); 
    SetWindowPos(hWnd, hWnd, dpiScaledX, dpiScaledY, dpiScaledWidth, dpiScaledHeight, SWP_NOZORDER | SWP_NOACTIVATE); 
} 
 
... 
 
case WM_CREATE: 
{ 
    // Add a button 
    HWND hWndChild = CreateWindow(L"BUTTON", L"Click Me",  
        WS_CHILD|WS_VISIBLE|BS_PUSHBUTTON, 
        0, 
        0, 
        0, 
        0, 
        hWnd, (HMENU)NULL, NULL, NULL); 
    if (hWndChild != NULL) 
    { 
        UpdateButtonLayoutForDpi(hWndChild); 
    } 
} 
break; 
 
case WM_DPICHANGED: 
{ 
    // Find the button and resize it 
    HWND hWndButton = FindWindowEx(hWnd, NULL, NULL, NULL); 
    if (hWndButton != NULL) 
    { 
        UpdateButtonLayoutForDpi(hWndButton); 
    } 
} 
break; 
```



<span data-ttu-id="09d2d-263">Lors de la mise à jour d’une application compatible DPI du système, voici quelques étapes courantes à suivre :</span><span class="sxs-lookup"><span data-stu-id="09d2d-263">When updating a System DPI-aware application, some common steps to follow are:</span></span>

1.  <span data-ttu-id="09d2d-264">Marquez le processus comme prenant en charge la résolution par moniteur (v2) à l’aide d’un manifeste d’application (ou d’une autre méthode, selon la ou les infrastructures d’interface utilisateur utilisées).</span><span class="sxs-lookup"><span data-stu-id="09d2d-264">Mark the process as per-monitor DPI aware (V2) using an application manifest (or other method, depending on the UI framework(s) used).</span></span>
2.  <span data-ttu-id="09d2d-265">Rendre la logique de disposition d’interface utilisateur réutilisable et la décaler du code d’initialisation de l’application de façon à ce qu’elle puisse être réutilisée en cas de changement de DPI (WM \_ DPICHANGED dans le cas de la programmation Windows (Win32)).</span><span class="sxs-lookup"><span data-stu-id="09d2d-265">Make UI layout logic reusable and move it out of application-initialization code such that it can be reused when a DPI change occurs (WM\_DPICHANGED in the case of Windows (Win32) programming).</span></span>
3.  <span data-ttu-id="09d2d-266">Invalidez tout code qui suppose que les données sensibles DPI (DPI/polices/tailles, etc.) n’ont jamais besoin d’être mises à jour.</span><span class="sxs-lookup"><span data-stu-id="09d2d-266">Invalidate any code that assumes that DPI-sensitive data (DPI/fonts/sizes/etc.) never need to be updated.</span></span> <span data-ttu-id="09d2d-267">Il est très courant de mettre en cache les tailles de police et les valeurs DPI lors de l’initialisation du processus.</span><span class="sxs-lookup"><span data-stu-id="09d2d-267">It is a very common practice to cache font sizes and DPI values at process initialization.</span></span> <span data-ttu-id="09d2d-268">Lors de la mise à jour d’une application pour qu’elle prenne en charge la résolution par moniteur, les données sensibles DPI doivent être réévaluées chaque fois qu’une nouvelle valeur PPP est rencontrée.</span><span class="sxs-lookup"><span data-stu-id="09d2d-268">When updating an application to become per-monitor DPI aware, DPI-sensitive data must be reevaluated whenever a new DPI is encountered.</span></span>
4.  <span data-ttu-id="09d2d-269">Lorsqu’un changement de PPP se produit, rechargez (ou re-pixellise) toutes les ressources bitmap pour la nouvelle résolution ou, éventuellement, la bitmap étirer les ressources actuellement chargées à la taille correcte.</span><span class="sxs-lookup"><span data-stu-id="09d2d-269">When a DPI change occurs, reload (or re-rasterize) any bitmap assets for the new DPI or, optionally, bitmap stretch the currently loaded assets to the correct size.</span></span>
5.  <span data-ttu-id="09d2d-270">Grep pour les API qui ne sont pas Per-Monitor compatibles PPP et les remplace par les API compatibles Per-Monitor DPI (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="09d2d-270">Grep for APIs that are not Per-Monitor DPI aware and replace them with Per-Monitor DPI-aware APIs (where applicable).</span></span> <span data-ttu-id="09d2d-271">Exemple : remplacez GetSystemMetrics par GetSystemMetricsForDpi.</span><span class="sxs-lookup"><span data-stu-id="09d2d-271">Example: replace GetSystemMetrics with GetSystemMetricsForDpi.</span></span>
6.  <span data-ttu-id="09d2d-272">Testez votre application sur un système multi-PPP ou à affichage multiple.</span><span class="sxs-lookup"><span data-stu-id="09d2d-272">Test your application on a multiple-display/multi-DPI system.</span></span>
7.  <span data-ttu-id="09d2d-273">Pour les fenêtres de niveau supérieur de votre application que vous ne pouvez pas mettre à jour avec une mise à l’échelle DPI correcte, utilisez la mise à l’échelle DPI en mode mixte (décrite ci-dessous) pour permettre l’étirement de la bitmap de ces fenêtres de niveau supérieur par le système.</span><span class="sxs-lookup"><span data-stu-id="09d2d-273">For any top-level windows in your application that you are unable to update to properly DPI scale, use mixed-mode DPI scaling (described below) to allow bitmap stretching of these top-level windows by the system.</span></span>

## <a name="mixed-mode-dpi-scaling-sub-process-dpi-scaling"></a><span data-ttu-id="09d2d-274">Mise à l’échelle PPP Mixed-Mode (mise à l’échelle PPP de sous-processus)</span><span class="sxs-lookup"><span data-stu-id="09d2d-274">Mixed-Mode DPI Scaling (Sub-Process DPI Scaling)</span></span>

<span data-ttu-id="09d2d-275">Lors de la mise à jour d’une application pour prendre en charge la prise en charge DPI par moniteur, il peut parfois devenir difficile ou impossible de mettre à jour chaque fenêtre de l’application en une seule fois.</span><span class="sxs-lookup"><span data-stu-id="09d2d-275">When updating an application to support per-monitor DPI awareness, it can sometimes become impractical or impossible to update every window in the application in one go.</span></span> <span data-ttu-id="09d2d-276">Cela peut simplement être dû au temps et à l’effort requis pour mettre à jour et tester toute l’interface utilisateur, ou parce que vous n’êtes pas propriétaire de tout le code d’interface utilisateur que vous devez exécuter (si votre application charge éventuellement une interface utilisateur tierce).</span><span class="sxs-lookup"><span data-stu-id="09d2d-276">This can simply be due to the time and effort required to update and test all UI, or because you do not own all of the UI code that you need to run (if your application perhaps loads third-party UI).</span></span> <span data-ttu-id="09d2d-277">Dans ce cas, Windows vous offre un moyen de faciliter le monde de la sensibilisation par moniteur en vous permettant d’exécuter certaines de vos fenêtres d’application (de niveau supérieur uniquement) dans leur mode de reconnaissance PPP d’origine, tout en mettant l’accent sur la mise à jour du temps et de l’énergie des parties les plus importantes de votre interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="09d2d-277">In these situations, Windows offers a way to ease into the world of per-monitor awareness by letting you run some of your application windows (top-level only) in their original DPI-awareness mode while you focus your time and energy updating the more important parts of your UI.</span></span>

<span data-ttu-id="09d2d-278">Voici une illustration de ce à quoi cela peut ressembler : vous mettez à jour l’interface utilisateur principale de votre application (« fenêtre principale » dans l’illustration) pour qu’elle s’exécute avec une prise en forme DPI par moniteur lorsque vous exécutez d’autres fenêtres dans leur mode existant (« fenêtre secondaire »).</span><span class="sxs-lookup"><span data-stu-id="09d2d-278">Below is an illustration of what this could look like: you update your main application UI ("Main Window"  in the illustration) to run with per-monitor DPI awareness while you run other windows in their existing mode ("Secondary Window").</span></span>

![différences de mise à l’échelle dpi entre les modes de sensibilisation](images/hub-page-illustrations.png)

<span data-ttu-id="09d2d-280">Avant la mise à jour anniversaire de Windows 10 (1607), le mode de reconnaissance PPP d’un processus était une propriété à l’échelle du processus.</span><span class="sxs-lookup"><span data-stu-id="09d2d-280">Prior to the Windows 10 Anniversary Update (1607), the DPI awareness mode of a process was a process-wide property.</span></span> <span data-ttu-id="09d2d-281">À compter de la mise à jour anniversaire Windows 10, cette propriété peut désormais être définie par fenêtre **de niveau supérieur** .</span><span class="sxs-lookup"><span data-stu-id="09d2d-281">Beginning in the Windows 10 Anniversary Update, this property can now be set per **top-level** window.</span></span> <span data-ttu-id="09d2d-282">(Les fenêtres **enfants** doivent continuer de correspondre à la taille de mise à l’échelle de leur parent.) Une fenêtre de niveau supérieur est définie en tant que fenêtre sans parent.</span><span class="sxs-lookup"><span data-stu-id="09d2d-282">(**Child** windows must continue to match the scaling size of their parent.) A top-level window is defined as a window with no parent.</span></span> <span data-ttu-id="09d2d-283">Il s’agit généralement d’une fenêtre « normale » avec des boutons de réduction, d’agrandissement et de fermeture.</span><span class="sxs-lookup"><span data-stu-id="09d2d-283">This is typically a "regular" window with minimize, maximize, and close buttons.</span></span> <span data-ttu-id="09d2d-284">Le scénario dans lequel la prise en charge DPI de sous-processus est destinée est d’avoir une interface utilisateur secondaire mise à l’échelle par Windows (bitmap étiré) tout en conservant le temps et les ressources nécessaires à la mise à jour de votre interface utilisateur principale.</span><span class="sxs-lookup"><span data-stu-id="09d2d-284">The scenario that sub-process DPI awareness is intended for is to have secondary UI scaled by Windows (bitmap stretched) while you focus your time and resources on updating your primary UI.</span></span>

<span data-ttu-id="09d2d-285">Pour activer la reconnaissance des PPP de sous-processus, appelez [**SetThreadDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext) avant et après les appels de création de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="09d2d-285">To enable sub-process DPI awareness, call [**SetThreadDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext) before and after any window creation calls.</span></span> <span data-ttu-id="09d2d-286">La fenêtre créée sera associée à la reconnaissance PPP que vous définissez via SetThreadDpiAwarenessContext.</span><span class="sxs-lookup"><span data-stu-id="09d2d-286">The window that is created will be associated with the DPI awareness that you set via SetThreadDpiAwarenessContext.</span></span> <span data-ttu-id="09d2d-287">Utilisez le deuxième appel pour restaurer la reconnaissance actuelle du thread s.</span><span class="sxs-lookup"><span data-stu-id="09d2d-287">Use the second call to restore the current thread s DPI awareness.</span></span>

<span data-ttu-id="09d2d-288">Si vous utilisez la mise à l’échelle DPI du sous-processus, vous pouvez vous appuyer sur Windows pour effectuer une partie de la mise à l’échelle DPI de votre application, ce qui peut augmenter la complexité de votre application.</span><span class="sxs-lookup"><span data-stu-id="09d2d-288">While using sub-process DPI scaling enables you to rely on Windows to do some of the DPI scaling for your application, it can increase the complexity of your application.</span></span> <span data-ttu-id="09d2d-289">Il est important de comprendre les inconvénients de cette approche et de la nature des complexités qu’elle introduite.</span><span class="sxs-lookup"><span data-stu-id="09d2d-289">It is important that you understand the drawbacks of this approach and nature of the complexities that it introduces.</span></span> <span data-ttu-id="09d2d-290">Pour plus d’informations sur la prise en charge DPI de sous-processus, consultez [mise à l’échelle dpi en mode mixte et API prenant en charge dpi.](high-dpi-improvements-for-desktop-applications.md)</span><span class="sxs-lookup"><span data-stu-id="09d2d-290">For more information about sub-process DPI awareness, see [Mixed-Mode DPI Scaling and DPI-aware APIs.](high-dpi-improvements-for-desktop-applications.md)</span></span>

## <a name="testing-your-changes"></a><span data-ttu-id="09d2d-291">Test de vos modifications</span><span class="sxs-lookup"><span data-stu-id="09d2d-291">Testing Your Changes</span></span>

<span data-ttu-id="09d2d-292">Une fois que vous avez mis à jour votre application pour qu’elle prenne en charge la résolution par moniteur, il est important de vérifier que votre application répond correctement aux modifications PPP dans un environnement à plusieurs résolutions.</span><span class="sxs-lookup"><span data-stu-id="09d2d-292">After you have updated your application to become per-monitor DPI aware, it is important to validate your application properly responds to DPI changes in a mixed-DPI environment.</span></span> <span data-ttu-id="09d2d-293">Voici quelques précisions à tester :</span><span class="sxs-lookup"><span data-stu-id="09d2d-293">Some specifics to test include:</span></span>

1.  <span data-ttu-id="09d2d-294">Déplacement de fenêtres d’application entre des affichages de valeurs PPP différentes</span><span class="sxs-lookup"><span data-stu-id="09d2d-294">Moving application windows back and forth between displays of different DPI values</span></span>
2.  <span data-ttu-id="09d2d-295">Démarrage de votre application sur des affichages de valeurs PPP différentes</span><span class="sxs-lookup"><span data-stu-id="09d2d-295">Starting your application on displays of different DPI values</span></span>
3.  <span data-ttu-id="09d2d-296">Modification du facteur d’échelle de votre moniteur pendant l’exécution de l’application</span><span class="sxs-lookup"><span data-stu-id="09d2d-296">Changing the scale factor for your monitor while the application is running</span></span>
4.  <span data-ttu-id="09d2d-297">Modifiez l’affichage que vous utilisez comme affichage principal, _déconnectez-vous de Windows_, puis retestez votre application après vous être connecté.</span><span class="sxs-lookup"><span data-stu-id="09d2d-297">Changing the display that you use as the primary display, _signing out of Windows_, then re-testing your application after signing back in.</span></span> <span data-ttu-id="09d2d-298">Cela est particulièrement utile pour rechercher du code qui utilise des tailles/Dimensions codées en dur.</span><span class="sxs-lookup"><span data-stu-id="09d2d-298">This is particularly useful in finding code that uses hard-coded sizes/dimensions.</span></span>

## <a name="common-pitfalls-win32"></a><span data-ttu-id="09d2d-299">Pièges courants (Win32)</span><span class="sxs-lookup"><span data-stu-id="09d2d-299">Common Pitfalls (Win32)</span></span>

<span data-ttu-id="09d2d-300">**N’utilise pas le rectangle suggéré fourni dans WM \_ DPICHANGED**</span><span class="sxs-lookup"><span data-stu-id="09d2d-300">**Not using the suggested rectangle that is provided in WM\_DPICHANGED**</span></span>

<span data-ttu-id="09d2d-301">Lorsque Windows envoie votre fenêtre d’application un message [**WM \_ DPICHANGED**](wm-dpichanged.md) , ce message comprend un rectangle suggéré que vous devez utiliser pour redimensionner votre fenêtre.</span><span class="sxs-lookup"><span data-stu-id="09d2d-301">When Windows sends your application window a [**WM\_DPICHANGED**](wm-dpichanged.md) message, this message includes a suggested rectangle that you should use to resize your window.</span></span> <span data-ttu-id="09d2d-302">Il est essentiel que votre application utilise ce rectangle pour se redimensionner, comme suit :</span><span class="sxs-lookup"><span data-stu-id="09d2d-302">It is critical that your application use this rectangle to resize itself, as this will:</span></span>

1.  <span data-ttu-id="09d2d-303">S’assurer que le curseur de la souris reste dans la même position relative sur la fenêtre lors du déplacement entre les affichages</span><span class="sxs-lookup"><span data-stu-id="09d2d-303">Ensure that the mouse cursor will stay in the same relative position on the Window when dragging between displays</span></span>
2.  <span data-ttu-id="09d2d-304">Empêchez la fenêtre d’application d’accéder à un cycle récursif PPP-modification, où une modification PPP déclenche une modification PPP ultérieure, ce qui déclenche une autre modification PPP.</span><span class="sxs-lookup"><span data-stu-id="09d2d-304">Prevent the application window from getting into a recursive dpi-change cycle where one DPI change triggers a subsequent DPI change, which triggers yet another DPI change.</span></span>

<span data-ttu-id="09d2d-305">Si vous avez des exigences spécifiques à l’application qui vous empêchent d’utiliser le rectangle suggéré fourni par Windows dans le \_ message WM DPICHANGED, consultez [**WM \_ GETDPISCALEDSIZE**](wm-getdpiscaledsize.md).</span><span class="sxs-lookup"><span data-stu-id="09d2d-305">If you have application-specific requirements that prevent you from using the suggested rectangle that Windows provides in the WM\_DPICHANGED message, see [**WM\_GETDPISCALEDSIZE**](wm-getdpiscaledsize.md).</span></span> <span data-ttu-id="09d2d-306">Ce message peut être utilisé pour attribuer à Windows une taille souhaitée que vous souhaitez utiliser une fois que le changement de DPI s’est produit, tout en évitant les problèmes décrits ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="09d2d-306">This message can be used to give Windows a desired size you'd like used once the DPI change has occurred, while still avoiding the issues described above.</span></span>

<span data-ttu-id="09d2d-307">**Absence de documentation sur la virtualisation**</span><span class="sxs-lookup"><span data-stu-id="09d2d-307">**Lack of documentation about virtualization**</span></span>

<span data-ttu-id="09d2d-308">Lorsqu’un HWND ou un processus s’exécute comme une prise en charge DPI ou une prise en charge DPI du système, il peut s’agir d’une image bitmap étirée par Windows.</span><span class="sxs-lookup"><span data-stu-id="09d2d-308">When an HWND or process is running as either DPI unaware or system DPI aware, it can be bitmap stretched by Windows.</span></span> <span data-ttu-id="09d2d-309">Dans ce cas, Windows met à l’échelle et convertit les informations PPP de certaines API vers l’espace de coordonnées du thread appelant.</span><span class="sxs-lookup"><span data-stu-id="09d2d-309">When this happens, Windows scales and converts DPI-sensitive information from some APIs to the coordinate space of the calling thread.</span></span> <span data-ttu-id="09d2d-310">Par exemple, si un thread qui ne prend pas en charge la résolution PPP interroge la taille de l’écran pendant qu’il s’exécute sur un affichage haute résolution, Windows virtualise la réponse fournie à l’application comme si l’écran était en unités de 96 ppp.</span><span class="sxs-lookup"><span data-stu-id="09d2d-310">For example, if a DPI-unaware thread queries the screen size while running on a high-DPI display, Windows will virtualize the answer given to the application as if the screen were in 96 DPI units.</span></span> <span data-ttu-id="09d2d-311">En guise d’alternative, lorsqu’un thread prenant en charge DPI système interagit avec un affichage à une résolution différente de celle utilisée lors du démarrage de la session de l’utilisateur actuel, Windows met à l’échelle certains appels d’API dans l’espace de coordonnées que le HWND utiliserait s’il s’exécutait à son facteur d’échelle PPP d’origine.</span><span class="sxs-lookup"><span data-stu-id="09d2d-311">Alternatively, when a System DPI-aware thread is interacting with a display at a different DPI than was in use when the current user's session was started, Windows will DPI-scale some API calls into the coordinate space that the HWND would be using if it were running at its original DPI scale factor.</span></span>

<span data-ttu-id="09d2d-312">Lorsque vous mettez à jour votre application de bureau avec une mise à l’échelle PPP correctement, il peut être difficile de savoir quels appels d’API peuvent retourner des valeurs virtualisées en fonction du contexte du thread. ces informations ne sont pas suffisamment documentées par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="09d2d-312">When you update your desktop application to DPI scale properly, it can difficult to know which API calls can return virtualized values based on the thread context; this information is not currently sufficiently documented by Microsoft.</span></span> <span data-ttu-id="09d2d-313">Sachez que si vous appelez une API système à partir d’un contexte de thread qui ne prend pas en charge DPI ou le système DPI, la valeur de retour peut être virtualisée.</span><span class="sxs-lookup"><span data-stu-id="09d2d-313">Be aware that if you call any system API from a DPI-unaware or system-DPI-aware thread context, the return value might be virtualized.</span></span> <span data-ttu-id="09d2d-314">Par conséquent, assurez-vous que votre thread s’exécute dans le contexte PPP que vous attendez quand vous interagissez avec l’écran ou des fenêtres individuelles.</span><span class="sxs-lookup"><span data-stu-id="09d2d-314">As such, make sure your thread is running in the DPI context you expect when interacting with the screen or individual windows.</span></span> <span data-ttu-id="09d2d-315">Lorsque vous modifiez temporairement le contexte PPP d’un thread à l’aide de [SetThreadDpiAwarenessContext](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext), veillez à restaurer l’ancien contexte lorsque vous avez terminé pour éviter de provoquer un comportement incorrect ailleurs dans votre application.</span><span class="sxs-lookup"><span data-stu-id="09d2d-315">When temporarily changing a thread's DPI context using [SetThreadDpiAwarenessContext](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext), be sure to restore the old context when you're done to avoid causing incorrect behavior elsewhere in your application.</span></span>

<span data-ttu-id="09d2d-316">**De nombreuses API Windows n’ont pas de contexte PPP**</span><span class="sxs-lookup"><span data-stu-id="09d2d-316">**Many Windows APIs do not have an DPI context**</span></span>

<span data-ttu-id="09d2d-317">De nombreuses API Windows héritées n’incluent pas de contexte PPP ou HWND dans le cadre de leur interface.</span><span class="sxs-lookup"><span data-stu-id="09d2d-317">Many legacy Windows APIs do not include a DPI or HWND context as part of their interface.</span></span> <span data-ttu-id="09d2d-318">Par conséquent, les développeurs doivent souvent effectuer des tâches supplémentaires pour gérer la mise à l’échelle des informations sensibles DPI, telles que les tailles, les points ou les icônes.</span><span class="sxs-lookup"><span data-stu-id="09d2d-318">As a result, developers often have to do additional work to handle the scaling of any DPI-sensitive information, such as sizes, points, or icons.</span></span> <span data-ttu-id="09d2d-319">Par exemple, les développeurs qui utilisent [LoadIcon](/windows/desktop/api/winuser/nf-winuser-loadiconw) doivent être chargés d’étirer les icônes de bitmap ou d’utiliser d’autres API pour charger les icônes correctement dimensionnées pour les PPP appropriées, telles que [LoadImage](/windows/desktop/api/winuser/nf-winuser-loadimagew).</span><span class="sxs-lookup"><span data-stu-id="09d2d-319">As an example, developers using [LoadIcon](/windows/desktop/api/winuser/nf-winuser-loadiconw) must either bitmap stretch loaded icons or use alternate APIs to load correctly-sized icons for the appropriate DPI, such as [LoadImage](/windows/desktop/api/winuser/nf-winuser-loadimagew).</span></span>

<span data-ttu-id="09d2d-320">**Réinitialisation forcée de la reconnaissance DPI à l’échelle du processus**</span><span class="sxs-lookup"><span data-stu-id="09d2d-320">**Forced reset of process-wide DPI awareness**</span></span>

<span data-ttu-id="09d2d-321">En général, le mode de reconnaissance PPP de votre processus ne peut pas être modifié après l’initialisation du processus.</span><span class="sxs-lookup"><span data-stu-id="09d2d-321">In general, the DPI awareness mode of your process cannot be changed after process initialization.</span></span> <span data-ttu-id="09d2d-322">Toutefois, Windows peut modifier de force le mode de reconnaissance DPI de votre processus si vous tentez de rompre la condition selon laquelle tous les HWND dans une arborescence de fenêtre ont le même mode de reconnaissance PPP.</span><span class="sxs-lookup"><span data-stu-id="09d2d-322">Windows can, however, forcibly change the DPI awareness mode of your process if you attempt to break the requirement that all HWNDs in a window tree have the same DPI awareness mode.</span></span> <span data-ttu-id="09d2d-323">Sur toutes les versions de Windows, à compter de Windows 10 1703, il n’est pas possible d’avoir des HWND différents dans une arborescence HWND qui s’exécutent dans différents modes de reconnaissance PPP.</span><span class="sxs-lookup"><span data-stu-id="09d2d-323">On all versions of Windows, as of Windows 10 1703, it is not possible to have different HWNDs in an HWND tree run in different DPI awareness modes.</span></span> <span data-ttu-id="09d2d-324">Si vous tentez de créer une relation enfant-parent qui interrompt cette règle, la prise en DPI de l’ensemble du processus peut être réinitialisée.</span><span class="sxs-lookup"><span data-stu-id="09d2d-324">If you attempt to create a child-parent relationship that breaks this rule, the DPI awareness of the entire process can be reset.</span></span> <span data-ttu-id="09d2d-325">Cela peut être déclenché par :</span><span class="sxs-lookup"><span data-stu-id="09d2d-325">This can be triggered by:</span></span>

1.  <span data-ttu-id="09d2d-326">Appel CreateWindow où la fenêtre parente passée est d’un mode de reconnaissance PPP différent du thread appelant.</span><span class="sxs-lookup"><span data-stu-id="09d2d-326">A CreateWindow call where the passed in parent window is of a different DPI awareness mode than the calling thread.</span></span>
2.  <span data-ttu-id="09d2d-327">Appel SetParent, où les deux fenêtres sont associées à différents modes de reconnaissance PPP.</span><span class="sxs-lookup"><span data-stu-id="09d2d-327">A SetParent call where the two windows are associated with different DPI awareness modes.</span></span>

<span data-ttu-id="09d2d-328">Le tableau ci-dessous montre ce qui se passe si vous tentez de violer cette règle :</span><span class="sxs-lookup"><span data-stu-id="09d2d-328">The table below shows what happens if you attempt to violate this rule:</span></span>



| <span data-ttu-id="09d2d-329">Opération</span><span class="sxs-lookup"><span data-stu-id="09d2d-329">Operation</span></span>                 | <span data-ttu-id="09d2d-330">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="09d2d-330">Windows 8.1</span></span>                                  | <span data-ttu-id="09d2d-331">Windows 10 (1607 et versions antérieures)</span><span class="sxs-lookup"><span data-stu-id="09d2d-331">Windows 10 (1607 and earlier)</span></span>                | <span data-ttu-id="09d2d-332">Windows 10 (1703 et versions ultérieures)</span><span class="sxs-lookup"><span data-stu-id="09d2d-332">Windows 10 (1703 and later)</span></span>                  |
|---------------------------|----------------------------------------------|----------------------------------------------|----------------------------------------------|
| <span data-ttu-id="09d2d-333">CreateWindow (in-proc)</span><span class="sxs-lookup"><span data-stu-id="09d2d-333">CreateWindow (In-Proc)</span></span>    | <span data-ttu-id="09d2d-334">N/A</span><span class="sxs-lookup"><span data-stu-id="09d2d-334">N/A</span></span>                                          | <span data-ttu-id="09d2d-335">**Héritages enfants** (mode mixte)</span><span class="sxs-lookup"><span data-stu-id="09d2d-335">**Child inherits** (mixed mode)</span></span>              | <span data-ttu-id="09d2d-336">**Héritages enfants** (mode mixte)</span><span class="sxs-lookup"><span data-stu-id="09d2d-336">**Child inherits** (mixed mode)</span></span>              |
| <span data-ttu-id="09d2d-337">CreateWindow (traitement croisé)</span><span class="sxs-lookup"><span data-stu-id="09d2d-337">CreateWindow (Cross-Proc)</span></span> | <span data-ttu-id="09d2d-338">**Réinitialisation forcée** (du processus de l’appelant)</span><span class="sxs-lookup"><span data-stu-id="09d2d-338">**Forced reset** (of caller's process)</span></span>       | <span data-ttu-id="09d2d-339">**Héritages enfants** (mode mixte)</span><span class="sxs-lookup"><span data-stu-id="09d2d-339">**Child inherits** (mixed mode)</span></span>              | <span data-ttu-id="09d2d-340">**Réinitialisation forcée** (du processus de l’appelant)</span><span class="sxs-lookup"><span data-stu-id="09d2d-340">**Forced reset** (of caller's process)</span></span>       |
| <span data-ttu-id="09d2d-341">SetParent, (in-proc)</span><span class="sxs-lookup"><span data-stu-id="09d2d-341">SetParent (In-Proc)</span></span>       | <span data-ttu-id="09d2d-342">N/A</span><span class="sxs-lookup"><span data-stu-id="09d2d-342">N/A</span></span>                                          | <span data-ttu-id="09d2d-343">**Réinitialisation forcée** (du processus en cours)</span><span class="sxs-lookup"><span data-stu-id="09d2d-343">**Forced reset** (of current process)</span></span>        | <span data-ttu-id="09d2d-344">**Fail** (état d’erreur \_ non valide \_ )</span><span class="sxs-lookup"><span data-stu-id="09d2d-344">**Fail** (ERROR\_INVALID\_STATE)</span></span>             |
| <span data-ttu-id="09d2d-345">SetParent, (traitement croisé)</span><span class="sxs-lookup"><span data-stu-id="09d2d-345">SetParent (Cross-Proc)</span></span>    | <span data-ttu-id="09d2d-346">**Réinitialisation forcée** (du processus de la fenêtre enfant)</span><span class="sxs-lookup"><span data-stu-id="09d2d-346">**Forced reset** (of child window's process)</span></span> | <span data-ttu-id="09d2d-347">**Réinitialisation forcée** (du processus de la fenêtre enfant)</span><span class="sxs-lookup"><span data-stu-id="09d2d-347">**Forced reset** (of child window's process)</span></span> | <span data-ttu-id="09d2d-348">**Réinitialisation forcée** (du processus de la fenêtre enfant)</span><span class="sxs-lookup"><span data-stu-id="09d2d-348">**Forced reset** (of child window's process)</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="09d2d-349">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="09d2d-349">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09d2d-350">Informations de référence sur les API haute résolution</span><span class="sxs-lookup"><span data-stu-id="09d2d-350">High DPI API Reference</span></span>](high-dpi-reference.md)
</dt> <dt>

[<span data-ttu-id="09d2d-351">La mise à l’échelle DPI en mode mixte et les API compatibles PPP.</span><span class="sxs-lookup"><span data-stu-id="09d2d-351">Mixed-Mode DPI Scaling and DPI-aware APIs.</span></span>](high-dpi-improvements-for-desktop-applications.md)
</dt> </dl>

