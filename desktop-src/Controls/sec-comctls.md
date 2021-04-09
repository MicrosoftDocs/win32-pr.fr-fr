---
title: Considérations sur la sécurité contrôles Microsoft Windows
description: Cette rubrique fournit des informations sur les considérations relatives à la sécurité pour les contrôles Windows.
ms.assetid: d5396fa1-452e-40e1-beaf-ae04690048f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e29ba986ddd1db980134f428c8abf152321617ef
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104102500"
---
# <a name="security-considerations-microsoft-windows-controls"></a><span data-ttu-id="06923-103">Considérations relatives à la sécurité : contrôles Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="06923-103">Security Considerations: Microsoft Windows Controls</span></span>

<span data-ttu-id="06923-104">Cette rubrique fournit des informations sur les considérations relatives à la sécurité pour les contrôles Windows.</span><span class="sxs-lookup"><span data-stu-id="06923-104">This topic provides information about security considerations related to the Windows controls.</span></span> <span data-ttu-id="06923-105">Les informations contenues dans cette rubrique ne fournissent pas tout ce que vous devez savoir sur les problèmes de sécurité. Utilisez-la comme point de départ et référence pour ce domaine technologique.</span><span class="sxs-lookup"><span data-stu-id="06923-105">The information in this topic does not provide all you need to know about security issues—use it as a starting point and reference for this technology area.</span></span>

<span data-ttu-id="06923-106">L’interconnexion entre les ordinateurs est courante. la principale préoccupation d’un développeur doit être la sécurité des applications.</span><span class="sxs-lookup"><span data-stu-id="06923-106">Interconnectivity among computers is common; a developer's chief concern must be application security.</span></span> <span data-ttu-id="06923-107">Les sections suivantes présentent certains problèmes de sécurité potentiels à prendre en compte lors de la programmation de contrôles Windows.</span><span class="sxs-lookup"><span data-stu-id="06923-107">The following sections discuss some potential security issues to consider when programming Windows controls.</span></span>

-   [<span data-ttu-id="06923-108">Messages de contrôle se terminant par null</span><span class="sxs-lookup"><span data-stu-id="06923-108">Null-terminated Control Messages</span></span>](#null-terminated-control-messages)
-   [<span data-ttu-id="06923-109">Utilisation de chaîne</span><span class="sxs-lookup"><span data-stu-id="06923-109">String Use</span></span>](#string-use)
-   [<span data-ttu-id="06923-110">Validation des entrées</span><span class="sxs-lookup"><span data-stu-id="06923-110">Input Validation</span></span>](#input-validation)
-   [<span data-ttu-id="06923-111">Utilisation du mot de passe</span><span class="sxs-lookup"><span data-stu-id="06923-111">Password Use</span></span>](#password-use)
-   [<span data-ttu-id="06923-112">alertes de sécurité</span><span class="sxs-lookup"><span data-stu-id="06923-112">Security Alerts</span></span>](#security-alerts)
-   [<span data-ttu-id="06923-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="06923-113">Related topics</span></span>](#related-topics)

## <a name="null-terminated-control-messages"></a><span data-ttu-id="06923-114">Messages de contrôle se terminant par null</span><span class="sxs-lookup"><span data-stu-id="06923-114">Null-terminated Control Messages</span></span>

<span data-ttu-id="06923-115">La plupart des messages de contrôle et des macros ont des paramètres de chaîne.</span><span class="sxs-lookup"><span data-stu-id="06923-115">Many of the control messages and macros have string parameters.</span></span> <span data-ttu-id="06923-116">Souvent, ces messages ne valident pas les chaînes d’entrée, en particulier, elles ne vérifient pas la fin d’une opération `'\0'` .</span><span class="sxs-lookup"><span data-stu-id="06923-116">Often these messages do not validate the input strings, in particular, they do not check for a terminating `'\0'`.</span></span> <span data-ttu-id="06923-117">Lorsque vous appelez un message qui utilise une chaîne comme paramètre, spécifiez explicitement que la chaîne se termine par un caractère null.</span><span class="sxs-lookup"><span data-stu-id="06923-117">When you call a message that uses a string as a parameter, explicitly specify that the string is null-terminated.</span></span>

## <a name="string-use"></a><span data-ttu-id="06923-118">Utilisation de chaîne</span><span class="sxs-lookup"><span data-stu-id="06923-118">String Use</span></span>

<span data-ttu-id="06923-119">Quand vous programmez des contrôles Windows, il est nécessaire de manipuler des chaînes.</span><span class="sxs-lookup"><span data-stu-id="06923-119">When you program Windows controls, it is necessary to manipulate strings.</span></span> <span data-ttu-id="06923-120">Presque tous les contrôles requièrent l’insertion de texte.</span><span class="sxs-lookup"><span data-stu-id="06923-120">Almost every control requires text to be inserted.</span></span> <span data-ttu-id="06923-121">Par exemple, pour remplir une zone de liste, vous devez charger des chaînes dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="06923-121">For example, to populate a list box you must load strings into the control.</span></span> <span data-ttu-id="06923-122">Étant donné que l’utilisation de chaînes de manière incorrecte provoque souvent des dépassements de mémoire tampon, prenez des précautions pour éviter ce risque de sécurité.</span><span class="sxs-lookup"><span data-stu-id="06923-122">Because using strings incorrectly often causes buffer overruns, take precautions to avoid this security risk.</span></span>

<span data-ttu-id="06923-123">Pour plus d’informations sur les dépassements de mémoire tampon, consultez *écriture de code sécurisé* par Michael Howard et David LeBlanc, Microsoft Press, 2002 et [meilleures pratiques pour les API de sécurité](/windows/desktop/SecBP/best-practices-for-the-security-apis).</span><span class="sxs-lookup"><span data-stu-id="06923-123">For more information about buffer overruns, see *Writing Secure Code* by Michael Howard and David LeBlanc, Microsoft Press, 2002 and [Best Practices for the Security APIs](/windows/desktop/SecBP/best-practices-for-the-security-apis).</span></span>

## <a name="input-validation"></a><span data-ttu-id="06923-124">Validation d'entrée</span><span class="sxs-lookup"><span data-stu-id="06923-124">Input Validation</span></span>

<span data-ttu-id="06923-125">Les messages de contrôle suivants peuvent présenter des problèmes de sécurité.</span><span class="sxs-lookup"><span data-stu-id="06923-125">The following control messages can present security problems.</span></span>

-   [<span data-ttu-id="06923-126">**\_GETLBTEXT CB**</span><span class="sxs-lookup"><span data-stu-id="06923-126">**CB\_GETLBTEXT**</span></span>](cb-getlbtext.md)
-   [<span data-ttu-id="06923-127">**\_GETISEARCHSTRING LVM**</span><span class="sxs-lookup"><span data-stu-id="06923-127">**LVM\_GETISEARCHSTRING**</span></span>](lvm-getisearchstring.md)
-   [<span data-ttu-id="06923-128">**SB \_ GETTEXT**</span><span class="sxs-lookup"><span data-stu-id="06923-128">**SB\_GETTEXT**</span></span>](sb-gettext.md)
-   [<span data-ttu-id="06923-129">**\_GETTIPTEXT SB**</span><span class="sxs-lookup"><span data-stu-id="06923-129">**SB\_GETTIPTEXT**</span></span>](sb-gettiptext.md)
-   [<span data-ttu-id="06923-130">**TO \_ GETBUTTONTEXT**</span><span class="sxs-lookup"><span data-stu-id="06923-130">**TB\_GETBUTTONTEXT**</span></span>](tb-getbuttontext.md)
-   [<span data-ttu-id="06923-131">**ATTÉNUATION \_ GETTEXT**</span><span class="sxs-lookup"><span data-stu-id="06923-131">**TTM\_GETTEXT**</span></span>](ttm-gettext.md)
-   [<span data-ttu-id="06923-132">**TVM \_ GETISEARCHSTRING**</span><span class="sxs-lookup"><span data-stu-id="06923-132">**TVM\_GETISEARCHSTRING**</span></span>](tvm-getisearchstring.md)

<span data-ttu-id="06923-133">Si le texte change entre l’appel pour obtenir la longueur du texte et l’heure d’affichage ou d’utilisation du texte, un dépassement de mémoire tampon peut se produire.</span><span class="sxs-lookup"><span data-stu-id="06923-133">If the text changes between the call to get the text length and the time the text is displayed or used, a buffer overrun can occur.</span></span> <span data-ttu-id="06923-134">Pour éviter cela, vous devez valider la chaîne avant de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="06923-134">To avoid this, you must validate the string before using it.</span></span> <span data-ttu-id="06923-135">En outre, les messages qui extraient Text, [**CB \_ GETLBTEXT**](cb-getlbtext.md), [**to \_ GETBUTTONTEXT**](tb-getbuttontext.md)et [**atténuation \_ GETTEXT**](ttm-gettext.md), n’ont pas de paramètre de taille de mémoire tampon qui présente le risque de dépassement de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="06923-135">In addition, the messages that retrieve text, [**CB\_GETLBTEXT**](cb-getlbtext.md), [**TB\_GETBUTTONTEXT**](tb-getbuttontext.md), and [**TTM\_GETTEXT**](ttm-gettext.md), have no buffer size parameter that presents the potential for a buffer overrun.</span></span>

<span data-ttu-id="06923-136">Quand vous utilisez [**CB \_ GETLBTEXT**](cb-getlbtext.md) ou [**SB \_ GETTEXT**](sb-gettext.md), vous devez d’abord appeler [**CB \_ GETLBTEXTLEN**](cb-getlbtextlen.md) ou [**SB \_ GETTEXTLENGTH**](sb-gettextlength.md) pour obtenir la taille de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="06923-136">When you use [**CB\_GETLBTEXT**](cb-getlbtext.md) or [**SB\_GETTEXT**](sb-gettext.md), you should first call [**CB\_GETLBTEXTLEN**](cb-getlbtextlen.md) or [**SB\_GETTEXTLENGTH**](sb-gettextlength.md) to obtain the buffer size.</span></span> <span data-ttu-id="06923-137">Certains de ces messages, [**to \_ GETBUTTONTEXT**](tb-getbuttontext.md), [**LVM \_ GETISEARCHSTRING**](lvm-getisearchstring.md)et [**TVM \_ GETISEARCHSTRING**](tvm-getisearchstring.md)peuvent être appelés avec une valeur de paramètre **null** pour obtenir la longueur de la chaîne avant d’appeler le message pour récupérer la chaîne.</span><span class="sxs-lookup"><span data-stu-id="06923-137">Some of these messages, [**TB\_GETBUTTONTEXT**](tb-getbuttontext.md), [**LVM\_GETISEARCHSTRING**](lvm-getisearchstring.md), and [**TVM\_GETISEARCHSTRING**](tvm-getisearchstring.md), can be called with a **NULL** parameter value to obtain the length of the string before invoking the message to retrieve the string.</span></span>

<span data-ttu-id="06923-138">Un message dont vous devez prêter une attention particulière est le message de la barre d’état [**SB \_ GETTIPTEXT**](sb-gettiptext.md) .</span><span class="sxs-lookup"><span data-stu-id="06923-138">A message that you should pay particular attention to is the status bar [**SB\_GETTIPTEXT**](sb-gettiptext.md) message.</span></span> <span data-ttu-id="06923-139">Ce message n’offre aucun moyen d’interroger la longueur de la chaîne qui doit être récupérée.</span><span class="sxs-lookup"><span data-stu-id="06923-139">This message provides no way to query the length of the string that is to be retrieved.</span></span>

## <a name="password-use"></a><span data-ttu-id="06923-140">Utilisation du mot de passe</span><span class="sxs-lookup"><span data-stu-id="06923-140">Password Use</span></span>

<span data-ttu-id="06923-141">Si vous utilisez des contrôles d’édition protégés par mot de passe (style [**\_ de mot de passe es**](edit-control-styles.md) ), la mémoire tampon qui contient le texte récupéré doit avoir la valeur zéro dès que possible pour éviter d’exposer le mot de passe de l’utilisateur en mémoire.</span><span class="sxs-lookup"><span data-stu-id="06923-141">If you use password-protected edit controls ([**ES\_PASSWORD**](edit-control-styles.md) style), the buffer that contains the retrieved text must be set to zero as soon as possible to avoid exposing the user's password in memory.</span></span>

## <a name="security-alerts"></a><span data-ttu-id="06923-142">Alertes de sécurité</span><span class="sxs-lookup"><span data-stu-id="06923-142">Security Alerts</span></span>

<span data-ttu-id="06923-143">Le tableau suivant répertorie les fonctionnalités qui, si elles sont utilisées de manière incorrecte, peuvent compromettre la sécurité de vos applications.</span><span class="sxs-lookup"><span data-stu-id="06923-143">The following table lists features that, if used incorrectly, can compromise the security of your applications.</span></span> <span data-ttu-id="06923-144">Les messages répertoriés ici ne fournissent pas de paramètre spécifiant la taille de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="06923-144">The messages listed here do not provide a parameter that specifies the buffer size.</span></span>



| <span data-ttu-id="06923-145">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="06923-145">Feature</span></span>                                               | <span data-ttu-id="06923-146">Limitation des risques</span><span class="sxs-lookup"><span data-stu-id="06923-146">Mitigation</span></span>                                                                                                                                              |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="06923-147">**DlgDirListComboBox**</span><span class="sxs-lookup"><span data-stu-id="06923-147">**DlgDirListComboBox**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dlgdirlistcomboboxa)      | <span data-ttu-id="06923-148">Assurez-vous que la mémoire tampon utilisée par la fonction peut être écrite dans et qu’elle se termine par un caractère null.</span><span class="sxs-lookup"><span data-stu-id="06923-148">Make sure the buffer used by the function can be written to and is null-terminated.</span></span>                                                                     |
| [<span data-ttu-id="06923-149">**\_GETLBTEXT CB**</span><span class="sxs-lookup"><span data-stu-id="06923-149">**CB\_GETLBTEXT**</span></span>](cb-getlbtext.md)                 | <span data-ttu-id="06923-150">Appelez [**CB \_ GETLBTEXTLEN**](cb-getlbtextlen.md) pour obtenir la taille de la mémoire tampon, puis appelez [**CB \_ GETLBTEXT**](cb-getlbtext.md) pour récupérer la chaîne.</span><span class="sxs-lookup"><span data-stu-id="06923-150">Call [**CB\_GETLBTEXTLEN**](cb-getlbtextlen.md) to obtain the buffer size, and then call [**CB\_GETLBTEXT**](cb-getlbtext.md) to retrieve the string.</span></span> |
| [<span data-ttu-id="06923-151">**\_GETISEARCHSTRING LVM**</span><span class="sxs-lookup"><span data-stu-id="06923-151">**LVM\_GETISEARCHSTRING**</span></span>](lvm-getisearchstring.md) | <span data-ttu-id="06923-152">Appelez le message avec une valeur de paramètre **null** pour obtenir la taille de la mémoire tampon, puis appelez le message une deuxième fois pour récupérer la chaîne.</span><span class="sxs-lookup"><span data-stu-id="06923-152">Call the message with a **NULL** parameter value to obtain the buffer size, and then call the message a second time to retrieve the string.</span></span>             |
| [<span data-ttu-id="06923-153">**SB \_ GETTEXT**</span><span class="sxs-lookup"><span data-stu-id="06923-153">**SB\_GETTEXT**</span></span>](sb-gettext.md)                     | <span data-ttu-id="06923-154">Appelez [**SB \_ GETTEXTLENGTH**](sb-gettextlength.md) pour obtenir la taille de la mémoire tampon, puis appelez [**SB \_ GETTEXT**](sb-gettext.md) pour récupérer la chaîne.</span><span class="sxs-lookup"><span data-stu-id="06923-154">Call [**SB\_GETTEXTLENGTH**](sb-gettextlength.md) to obtain the buffer size, and then call [**SB\_GETTEXT**](sb-gettext.md) to retrieve the string.</span></span>   |
| [<span data-ttu-id="06923-155">**TO \_ GETBUTTONTEXT**</span><span class="sxs-lookup"><span data-stu-id="06923-155">**TB\_GETBUTTONTEXT**</span></span>](tb-getbuttontext.md)         | <span data-ttu-id="06923-156">Appelez le message avec une valeur de paramètre **null** pour obtenir la taille de la mémoire tampon, puis appelez le message une deuxième fois pour récupérer la chaîne.</span><span class="sxs-lookup"><span data-stu-id="06923-156">Call the message with a **NULL** parameter value to obtain the buffer size, and then call the message a second time to retrieve the string.</span></span>             |
| [<span data-ttu-id="06923-157">**ATTÉNUATION \_ GETTEXT**</span><span class="sxs-lookup"><span data-stu-id="06923-157">**TTM\_GETTEXT**</span></span>](ttm-gettext.md)                   | <span data-ttu-id="06923-158">Ce message n’offre aucun moyen de connaître ou de spécifier la taille de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="06923-158">This message does not provide a way for you to know or specify the size of the buffer.</span></span>                                                                  |
| [<span data-ttu-id="06923-159">**TVM \_ GETISEARCHSTRING**</span><span class="sxs-lookup"><span data-stu-id="06923-159">**TVM\_GETISEARCHSTRING**</span></span>](tvm-getisearchstring.md) | <span data-ttu-id="06923-160">Appelez le message en passant une valeur de paramètre **null** pour obtenir la taille de la mémoire tampon, puis appelez le message une seconde fois pour récupérer la chaîne.</span><span class="sxs-lookup"><span data-stu-id="06923-160">Call the message by passing a **NULL** parameter value to obtain the buffer size, and then call the message a second time to retrieve the string.</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="06923-161">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="06923-161">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="06923-162">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="06923-162">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="06923-163">Sécurité Microsoft</span><span class="sxs-lookup"><span data-stu-id="06923-163">Microsoft Security</span></span>](https://www.microsoft.com/security/default.aspx)
</dt> <dt>

[<span data-ttu-id="06923-164">Sécurité</span><span class="sxs-lookup"><span data-stu-id="06923-164">Security</span></span>](/windows/desktop/security)
</dt> <dt>

[<span data-ttu-id="06923-165">Ressources de sécurité TechNet</span><span class="sxs-lookup"><span data-stu-id="06923-165">TechNet Security Resources</span></span>](https://www.microsoft.com/technet/security/Bulletin/MS10-059.mspx)
</dt> <dt>

[<span data-ttu-id="06923-166">Meilleures pratiques pour les API de sécurité</span><span class="sxs-lookup"><span data-stu-id="06923-166">Best Practices for the Security APIs</span></span>](/windows/desktop/SecBP/best-practices-for-the-security-apis)
</dt> </dl>

 

 