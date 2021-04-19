---
title: Paramètres des Rapports d’erreurs Windows
description: Paramètres pour personnaliser l’expérience de signalement des problèmes. Tous ces paramètres peuvent être définis à l’aide de stratégie de groupe. Certains peuvent également être modifiés dans le centre de maintenance pour Windows 7 et Windows 8. Pour Windows 10, utilisez la fonction de recherche dans paramètres pour localiser afficher les paramètres système avancés.
ms.assetid: 031c5591-31b0-42f1-9a98-ecf10a5d5571
keywords:
- Rapport d’erreurs Windows du rapport d’erreurs Windows, paramètres
ms.topic: article
ms.date: 03/12/2021
ms.openlocfilehash: 28b6abbda7d851daddb75ec534b8128d1a831b3f
ms.sourcegitcommit: 434d5437d4c31c47358598ea5275177c2698f557
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/13/2021
ms.locfileid: "106532414"
---
# <a name="wer-settings"></a><span data-ttu-id="d2738-107">Paramètres des Rapports d’erreurs Windows</span><span class="sxs-lookup"><span data-stu-id="d2738-107">WER Settings</span></span>

<span data-ttu-id="d2738-108">Rapport d’erreurs Windows (WER) fournit de nombreux paramètres pour personnaliser l’expérience de signalement des problèmes.</span><span class="sxs-lookup"><span data-stu-id="d2738-108">Windows Error Reporting (WER) provides many settings to customize the problem reporting experience.</span></span> <span data-ttu-id="d2738-109">Tous ces paramètres peuvent être définis à l’aide de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="d2738-109">All of these settings can be set using Group Policy.</span></span> <span data-ttu-id="d2738-110">Certains peuvent également être modifiés dans le **Centre de maintenance** pour Windows 7 et Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d2738-110">Some can also be changed in **Action Center** for Windows 7 and Windows 8.</span></span> <span data-ttu-id="d2738-111">Pour Windows 10, utilisez la fonction de recherche dans paramètres pour localiser **afficher les paramètres système avancés**.</span><span class="sxs-lookup"><span data-stu-id="d2738-111">For Windows 10, use the search function in Settings to locate **View advanced system settings**.</span></span> <span data-ttu-id="d2738-112">Les paramètres WER se trouvent dans l’une des sous-clés de Registre suivantes :</span><span class="sxs-lookup"><span data-stu-id="d2738-112">WER settings are located in one of the following registry subkeys:</span></span>

-   <span data-ttu-id="d2738-113">**HKEY \_ Logiciel \_ utilisateur actuel** \\  \\ **Microsoft** \\ **Windows** \\ **rapport d’erreurs Windows**</span><span class="sxs-lookup"><span data-stu-id="d2738-113">**HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Windows**\\**Windows Error Reporting**</span></span>
-   <span data-ttu-id="d2738-114">**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **Windows** \\ **rapport d’erreurs Windows**</span><span class="sxs-lookup"><span data-stu-id="d2738-114">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Windows**\\**Windows Error Reporting**</span></span>

## <a name="windows-error-reporting-subkey"></a><span data-ttu-id="d2738-115">Sous-clé Rapport d’erreurs Windows</span><span class="sxs-lookup"><span data-stu-id="d2738-115">Windows Error Reporting subkey</span></span>

<dl> <dt>

<span data-ttu-id="d2738-116"><span id="BypassDataThrottling"></span><span id="bypassdatathrottling"></span><span id="BYPASSDATATHROTTLING"></span>**BypassDataThrottling**</span><span class="sxs-lookup"><span data-stu-id="d2738-116"><span id="BypassDataThrottling"></span><span id="bypassdatathrottling"></span><span id="BYPASSDATATHROTTLING"></span>**BypassDataThrottling**</span></span>
</dt> <dd>

<span data-ttu-id="d2738-117">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="d2738-117">**REG\_DWORD**</span></span>

<span data-ttu-id="d2738-118">Valeurs possibles :</span><span class="sxs-lookup"><span data-stu-id="d2738-118">Possible values:</span></span><dl> <dd>

<span data-ttu-id="d2738-119">0-désactiver la limitation de contournement de données.</span><span class="sxs-lookup"><span data-stu-id="d2738-119">0 - Disable data bypass throttling.</span></span> <span data-ttu-id="d2738-120">Si le contournement est désactivé ou n’est pas configuré en tant que paramètre de stratégie, WER limite les données par défaut.</span><span class="sxs-lookup"><span data-stu-id="d2738-120">If the bypass is disabled or not configured as a policy setting, WER throttles data by default.</span></span> <span data-ttu-id="d2738-121">WER ne télécharge pas plus d’un fichier CAB pour un rapport qui contient des données sur les mêmes types d’événements.</span><span class="sxs-lookup"><span data-stu-id="d2738-121">WER does not upload more than one CAB file for a report that contains data about the same event types.</span></span>

</dd> <dd>

<span data-ttu-id="d2738-122">1-activer la limitation de contournement des données.</span><span class="sxs-lookup"><span data-stu-id="d2738-122">1 - Enable data bypass throttling.</span></span> <span data-ttu-id="d2738-123">WER ne limite pas les données.</span><span class="sxs-lookup"><span data-stu-id="d2738-123">WER does not throttle data.</span></span> <span data-ttu-id="d2738-124">WER télécharge des fichiers CAB supplémentaires qui peuvent contenir des données sur les mêmes types d’événements qu’un rapport téléchargé précédemment.</span><span class="sxs-lookup"><span data-stu-id="d2738-124">WER uploads additional CAB files that can contain data about the same event types as an earlier uploaded report.</span></span>

</dd> </dl>

<span data-ttu-id="d2738-125">Indique s’il faut activer le contournement de la limitation des données du client WER</span><span class="sxs-lookup"><span data-stu-id="d2738-125">Whether to enable the bypass of WER client data throttling</span></span>

</dd> <dt>

<span data-ttu-id="d2738-126"><span id="ConfigureArchive"></span><span id="configurearchive"></span><span id="CONFIGUREARCHIVE"></span>**ConfigureArchive**</span><span class="sxs-lookup"><span data-stu-id="d2738-126"><span id="ConfigureArchive"></span><span id="configurearchive"></span><span id="CONFIGUREARCHIVE"></span>**ConfigureArchive**</span></span>
</dt> <dd>

<span data-ttu-id="d2738-127">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="d2738-127">**REG\_DWORD**</span></span>

<span data-ttu-id="d2738-128">Valeurs possibles :</span><span class="sxs-lookup"><span data-stu-id="d2738-128">Possible values:</span></span><dl> <dd><span data-ttu-id="d2738-129">1-paramètres uniquement (par défaut sur Windows 7)</span><span class="sxs-lookup"><span data-stu-id="d2738-129">1 - Parameters only (default on Windows 7)</span></span></dd> <dd><span data-ttu-id="d2738-130">2-toutes les données (par défaut sur Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="d2738-130">2 - All data (default on Windows Vista)</span></span></dd> </dl>

<span data-ttu-id="d2738-131">Indique s’il faut archiver les paramètres uniquement ou toutes les données</span><span class="sxs-lookup"><span data-stu-id="d2738-131">Whether to archive parameters only or all data</span></span>

</dd> <dt>

<span data-ttu-id="d2738-132"><span id="Consent_DefaultConsent"></span><span id="consent_defaultconsent"></span><span id="CONSENT_DEFAULTCONSENT"></span>**DefaultConsent de consentement \\**</span><span class="sxs-lookup"><span data-stu-id="d2738-132"><span id="Consent_DefaultConsent"></span><span id="consent_defaultconsent"></span><span id="CONSENT_DEFAULTCONSENT"></span>**Consent\\DefaultConsent**</span></span>
</dt> <dd>

<span data-ttu-id="d2738-133">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="d2738-133">**REG\_DWORD**</span></span>

<span data-ttu-id="d2738-134">Valeurs possibles :</span><span class="sxs-lookup"><span data-stu-id="d2738-134">Possible values:</span></span><dl> <dd><span data-ttu-id="d2738-135">1-toujours demander (par défaut)</span><span class="sxs-lookup"><span data-stu-id="d2738-135">1 - Always ask (default)</span></span></dd> <dd><span data-ttu-id="d2738-136">2-paramètres uniquement</span><span class="sxs-lookup"><span data-stu-id="d2738-136">2 - Parameters only</span></span></dd> <dd><span data-ttu-id="d2738-137">3-paramètres et données sécurisées</span><span class="sxs-lookup"><span data-stu-id="d2738-137">3 - Parameters and safe data</span></span></dd> <dd><span data-ttu-id="d2738-138">4-toutes les données</span><span class="sxs-lookup"><span data-stu-id="d2738-138">4 - All data</span></span></dd> </dl>

<span data-ttu-id="d2738-139">Choix de consentement par défaut</span><span class="sxs-lookup"><span data-stu-id="d2738-139">Default consent choice</span></span>

</dd> <dt>

<span data-ttu-id="d2738-140"><span id="Consent_DefaultOverrideBehavior"></span><span id="consent_defaultoverridebehavior"></span><span id="CONSENT_DEFAULTOVERRIDEBEHAVIOR"></span>**DefaultOverrideBehavior de consentement \\**</span><span class="sxs-lookup"><span data-stu-id="d2738-140"><span id="Consent_DefaultOverrideBehavior"></span><span id="consent_defaultoverridebehavior"></span><span id="CONSENT_DEFAULTOVERRIDEBEHAVIOR"></span>**Consent\\DefaultOverrideBehavior**</span></span>
</dt> <dd>

<span data-ttu-id="d2738-141">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="d2738-141">**REG\_DWORD**</span></span>

<span data-ttu-id="d2738-142">Valeurs possibles :</span><span class="sxs-lookup"><span data-stu-id="d2738-142">Possible values:</span></span><dl> <dd><span data-ttu-id="d2738-143">0-le consentement vertical remplace le consentement par défaut (par défaut)</span><span class="sxs-lookup"><span data-stu-id="d2738-143">0 - Vertical consent will override the default consent (default)</span></span></dd> <dd><span data-ttu-id="d2738-144">1-le consentement par défaut remplacera le consentement propre à l’application</span><span class="sxs-lookup"><span data-stu-id="d2738-144">1 - Default consent will override the application-specific consent</span></span></dd> </dl>

<span data-ttu-id="d2738-145">Indique si le consentement par défaut remplace le consentement vertical</span><span class="sxs-lookup"><span data-stu-id="d2738-145">Whether default consent overrides vertical consent</span></span>

</dd> <dt>

<span data-ttu-id="d2738-146"><span id="Consent__VerticalName_"></span><span id="consent__verticalname_"></span><span id="CONSENT__VERTICALNAME_"></span>**VerticalName de consentement \\ \[\]**</span><span class="sxs-lookup"><span data-stu-id="d2738-146"><span id="Consent__VerticalName_"></span><span id="consent__verticalname_"></span><span id="CONSENT__VERTICALNAME_"></span>**Consent\\\[VerticalName\]**</span></span>
</dt> <dd>

<span data-ttu-id="d2738-147">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="d2738-147">**REG\_DWORD**</span></span>

<span data-ttu-id="d2738-148">Valeurs possibles :</span><span class="sxs-lookup"><span data-stu-id="d2738-148">Possible values:</span></span><dl> <dd><span data-ttu-id="d2738-149">1-toujours demander (par défaut)</span><span class="sxs-lookup"><span data-stu-id="d2738-149">1 - Always ask (default)</span></span></dd> <dd><span data-ttu-id="d2738-150">2-paramètres uniquement</span><span class="sxs-lookup"><span data-stu-id="d2738-150">2 - Parameters only</span></span></dd> <dd><span data-ttu-id="d2738-151">3-paramètres et données sécurisées</span><span class="sxs-lookup"><span data-stu-id="d2738-151">3 - Parameters and safe data</span></span></dd> <dd><span data-ttu-id="d2738-152">4-toutes les données</span><span class="sxs-lookup"><span data-stu-id="d2738-152">4 - All data</span></span></dd> </dl>

<span data-ttu-id="d2738-153">Choix du consentement pour le plug-in WER</span><span class="sxs-lookup"><span data-stu-id="d2738-153">Consent choice for the WER plug-in</span></span>

</dd> <dt>

<span data-ttu-id="d2738-154"><span id="CorporateWERDirectory"></span><span id="corporatewerdirectory"></span><span id="CORPORATEWERDIRECTORY"></span>**CorporateWERDirectory**</span><span class="sxs-lookup"><span data-stu-id="d2738-154"><span id="CorporateWERDirectory"></span><span id="corporatewerdirectory"></span><span id="CORPORATEWERDIRECTORY"></span>**CorporateWERDirectory**</span></span>
</dt> <dd>

<span data-ttu-id="d2738-155">**SZ de REG \_**</span><span class="sxs-lookup"><span data-stu-id="d2738-155">**REG\_SZ**</span></span>

<span data-ttu-id="d2738-156">Chemin d’accès au répertoire</span><span class="sxs-lookup"><span data-stu-id="d2738-156">The directory path</span></span>

<span data-ttu-id="d2738-157">Répertoire cible sur le serveur</span><span class="sxs-lookup"><span data-stu-id="d2738-157">Target directory on the server</span></span>

</dd> <dt>

<span data-ttu-id="d2738-158"><span id="CorporateWERPortNumber"></span><span id="corporatewerportnumber"></span><span id="CORPORATEWERPORTNUMBER"></span>**CorporateWERPortNumber**</span><span class="sxs-lookup"><span data-stu-id="d2738-158"><span id="CorporateWERPortNumber"></span><span id="corporatewerportnumber"></span><span id="CORPORATEWERPORTNUMBER"></span>**CorporateWERPortNumber**</span></span>
</dt> <dd>

<span data-ttu-id="d2738-159">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="d2738-159">**REG\_DWORD**</span></span>

<span data-ttu-id="d2738-160">Le numéro de port</span><span class="sxs-lookup"><span data-stu-id="d2738-160">The port number</span></span>

<span data-ttu-id="d2738-161">Numéro de port à utiliser avec le serveur d’entreprise</span><span class="sxs-lookup"><span data-stu-id="d2738-161">Port number to be used with the corporate server</span></span>

</dd> <dt>

<span data-ttu-id="d2738-162"><span id="CorporateWERServer"></span><span id="corporatewerserver"></span><span id="CORPORATEWERSERVER"></span>**CorporateWERServer**</span><span class="sxs-lookup"><span data-stu-id="d2738-162"><span id="CorporateWERServer"></span><span id="corporatewerserver"></span><span id="CORPORATEWERSERVER"></span>**CorporateWERServer**</span></span>
</dt> <dd>

<span data-ttu-id="d2738-163">**SZ de REG \_**</span><span class="sxs-lookup"><span data-stu-id="d2738-163">**REG\_SZ**</span></span>

<span data-ttu-id="d2738-164">Le nom du serveur</span><span class="sxs-lookup"><span data-stu-id="d2738-164">The name of the server</span></span>

<span data-ttu-id="d2738-165">Nom du serveur d’entreprise</span><span class="sxs-lookup"><span data-stu-id="d2738-165">Corporate server name</span></span>

</dd> <dt>

<span data-ttu-id="d2738-166"><span id="CorporateWERUseAuthentication"></span><span id="corporateweruseauthentication"></span><span id="CORPORATEWERUSEAUTHENTICATION"></span>**CorporateWERUseAuthentication**</span><span class="sxs-lookup"><span data-stu-id="d2738-166"><span id="CorporateWERUseAuthentication"></span><span id="corporateweruseauthentication"></span><span id="CORPORATEWERUSEAUTHENTICATION"></span>**CorporateWERUseAuthentication**</span></span>
</dt> <dd>

<span data-ttu-id="d2738-167">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="d2738-167">**REG\_DWORD**</span></span>

<span data-ttu-id="d2738-168">Valeurs possibles :</span><span class="sxs-lookup"><span data-stu-id="d2738-168">Possible values:</span></span><dl> <dd><span data-ttu-id="d2738-169">0-non (valeur par défaut)</span><span class="sxs-lookup"><span data-stu-id="d2738-169">0 - No (default)</span></span></dd> <dd><span data-ttu-id="d2738-170">1 - Oui</span><span class="sxs-lookup"><span data-stu-id="d2738-170">1 - Yes</span></span></dd> </dl>

<span data-ttu-id="d2738-171">Indique s’il faut utiliser l’authentification intégrée de Windows</span><span class="sxs-lookup"><span data-stu-id="d2738-171">Whether to use Windows Integrated Authentication</span></span>

</dd> <dt>

<span data-ttu-id="d2738-172"><span id="CorporateWERUseSSL"></span><span id="corporatewerusessl"></span><span id="CORPORATEWERUSESSL"></span>**CorporateWERUseSSL**</span><span class="sxs-lookup"><span data-stu-id="d2738-172"><span id="CorporateWERUseSSL"></span><span id="corporatewerusessl"></span><span id="CORPORATEWERUSESSL"></span>**CorporateWERUseSSL**</span></span>
</dt> <dd>

<span data-ttu-id="d2738-173">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="d2738-173">**REG\_DWORD**</span></span>

<span data-ttu-id="d2738-174">Valeurs possibles :</span><span class="sxs-lookup"><span data-stu-id="d2738-174">Possible values:</span></span><dl> <dd><span data-ttu-id="d2738-175">0-non (valeur par défaut)</span><span class="sxs-lookup"><span data-stu-id="d2738-175">0 - No (default)</span></span></dd> <dd><span data-ttu-id="d2738-176">1 - Oui</span><span class="sxs-lookup"><span data-stu-id="d2738-176">1 - Yes</span></span></dd> </dl>

<span data-ttu-id="d2738-177">Indique s’il faut utiliser SSL</span><span class="sxs-lookup"><span data-stu-id="d2738-177">Whether to use SSL</span></span>

</dd> <dt>

<span data-ttu-id="d2738-178"><span id="DebugApplications__ExeName___replace___ExeName___with_an_actual_name_of_an_.exe_file__for_example___notepad.exe__"></span><span id="debugapplications__exename___replace___exename___with_an_actual_name_of_an_.exe_file__for_example___notepad.exe__"></span><span id="DEBUGAPPLICATIONS__EXENAME___REPLACE___EXENAME___WITH_AN_ACTUAL_NAME_OF_AN_.EXE_FILE__FOR_EXAMPLE___NOTEPAD.EXE__"></span>**DebugApplications \\ \[ exeName \] (remplacez « \[ exeName \] » par le nom réel d’un fichier. exe, par exemple, « notepad.exe »)**</span><span class="sxs-lookup"><span data-stu-id="d2738-178"><span id="DebugApplications__ExeName___replace___ExeName___with_an_actual_name_of_an_.exe_file__for_example___notepad.exe__"></span><span id="debugapplications__exename___replace___exename___with_an_actual_name_of_an_.exe_file__for_example___notepad.exe__"></span><span id="DEBUGAPPLICATIONS__EXENAME___REPLACE___EXENAME___WITH_AN_ACTUAL_NAME_OF_AN_.EXE_FILE__FOR_EXAMPLE___NOTEPAD.EXE__"></span>**DebugApplications\\\[ExeName\] (replace "\[ExeName\]" with an actual name of an .exe file, for example, "notepad.exe")**</span></span>
</dt> <dd>

<span data-ttu-id="d2738-179">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="d2738-179">**REG\_DWORD**</span></span>

<span data-ttu-id="d2738-180">Valeurs possibles :</span><span class="sxs-lookup"><span data-stu-id="d2738-180">Possible values:</span></span>

<dl> <dd><span data-ttu-id="d2738-181">0-les processus avec un nom d’image exécutable de **\[ exeName \]** ne nécessitent pas que l’utilisateur choisisse **Déboguer** ou **Continuer** (par défaut)</span><span class="sxs-lookup"><span data-stu-id="d2738-181">0 - Processes with an executable image name of **\[ExeName\]** do not require the user to choose **Debug** or **Continue** (default)</span></span></dd> <dd><span data-ttu-id="d2738-182">1-les processus avec un nom d’image exécutable de **\[ exeName \]** obligent l’utilisateur à choisir **Déboguer** ou **Continuer**</span><span class="sxs-lookup"><span data-stu-id="d2738-182">1 - Processes with an executable image name of **\[ExeName\]** require the user to choose **Debug** or **Continue**</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="d2738-183"><span id="DebugApplications________is_the_literal_value_name_"></span><span id="debugapplications________is_the_literal_value_name_"></span><span id="DEBUGAPPLICATIONS________IS_THE_LITERAL_VALUE_NAME_"></span>**DebugApplications \\ \* (" \* " est le nom de la valeur littérale)**</span><span class="sxs-lookup"><span data-stu-id="d2738-183"><span id="DebugApplications________is_the_literal_value_name_"></span><span id="debugapplications________is_the_literal_value_name_"></span><span id="DEBUGAPPLICATIONS________IS_THE_LITERAL_VALUE_NAME_"></span>**DebugApplications\\\* ("\*" is the literal value name)**</span></span>
</dt> <dd>

<span data-ttu-id="d2738-184">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="d2738-184">**REG\_DWORD**</span></span>

<span data-ttu-id="d2738-185">Valeurs possibles :</span><span class="sxs-lookup"><span data-stu-id="d2738-185">Possible values:</span></span>

<dl> <dd><span data-ttu-id="d2738-186">0-tous les processus à l’exception de ceux spécifiés explicitement dans le paramètre **DebugApplications \\ \[ \] exeName** ne nécessitent pas que l’utilisateur choisisse **Debug** ou **continue** (valeur par défaut)</span><span class="sxs-lookup"><span data-stu-id="d2738-186">0 - All processes except ones specified explicitly in the setting **DebugApplications\\\[ExeName\]** do not require the user to choose **Debug** or **Continue** (default)</span></span></dd> <dd><span data-ttu-id="d2738-187">1-tous les processus à l’exception de ceux spécifiés explicitement dans le paramètre **DebugApplications \\ \[ exeName \]** obligent l’utilisateur à choisir **Déboguer** ou **Continuer**</span><span class="sxs-lookup"><span data-stu-id="d2738-187">1 - All processes except ones specified explicitly in the setting **DebugApplications\\\[ExeName\]** require the user to choose **Debug** or **Continue**</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="d2738-188"><span id="DisableArchive"></span><span id="disablearchive"></span><span id="DISABLEARCHIVE"></span>**DisableArchive**</span><span class="sxs-lookup"><span data-stu-id="d2738-188"><span id="DisableArchive"></span><span id="disablearchive"></span><span id="DISABLEARCHIVE"></span>**DisableArchive**</span></span>
</dt> <dd>

<span data-ttu-id="d2738-189">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="d2738-189">**REG\_DWORD**</span></span>

<span data-ttu-id="d2738-190">Valeurs possibles :</span><span class="sxs-lookup"><span data-stu-id="d2738-190">Possible values:</span></span><dl> <dd><span data-ttu-id="d2738-191">0 - Activé</span><span class="sxs-lookup"><span data-stu-id="d2738-191">0 - Enabled</span></span></dd> <dd><span data-ttu-id="d2738-192">1 - Désactivé</span><span class="sxs-lookup"><span data-stu-id="d2738-192">1 - Disabled</span></span></dd> </dl>

<span data-ttu-id="d2738-193">Activer ou désactiver l’archive</span><span class="sxs-lookup"><span data-stu-id="d2738-193">Enable or disable the archive</span></span>

</dd> <dt>

<span data-ttu-id="d2738-194"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Activée**</span><span class="sxs-lookup"><span data-stu-id="d2738-194"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="d2738-195">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="d2738-195">**REG\_DWORD**</span></span>

<span data-ttu-id="d2738-196">Valeurs possibles :</span><span class="sxs-lookup"><span data-stu-id="d2738-196">Possible values:</span></span><dl> <dd><span data-ttu-id="d2738-197">0-activé (valeur par défaut)</span><span class="sxs-lookup"><span data-stu-id="d2738-197">0 - Enabled (default)</span></span></dd> <dd><span data-ttu-id="d2738-198">1 - Désactivé</span><span class="sxs-lookup"><span data-stu-id="d2738-198">1 - Disabled</span></span></dd> </dl>

<span data-ttu-id="d2738-199">Activer ou désactiver le WER</span><span class="sxs-lookup"><span data-stu-id="d2738-199">Enable or disable WER</span></span>

</dd> <dt>

<span data-ttu-id="d2738-200"><span id="DisableQueue"></span><span id="disablequeue"></span><span id="DISABLEQUEUE"></span>**DisableQueue**</span><span class="sxs-lookup"><span data-stu-id="d2738-200"><span id="DisableQueue"></span><span id="disablequeue"></span><span id="DISABLEQUEUE"></span>**DisableQueue**</span></span>
</dt> <dd>

<span data-ttu-id="d2738-201">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="d2738-201">**REG\_DWORD**</span></span>

<span data-ttu-id="d2738-202">Valeurs possibles :</span><span class="sxs-lookup"><span data-stu-id="d2738-202">Possible values:</span></span><dl> <dd><span data-ttu-id="d2738-203">0 - Activé</span><span class="sxs-lookup"><span data-stu-id="d2738-203">0 - Enabled</span></span></dd> <dd><span data-ttu-id="d2738-204">1 - Désactivé</span><span class="sxs-lookup"><span data-stu-id="d2738-204">1 - Disabled</span></span></dd> </dl>

<span data-ttu-id="d2738-205">Activer ou désactiver la mise en file d’attente de rapports</span><span class="sxs-lookup"><span data-stu-id="d2738-205">Enable or disable report queuing</span></span>

</dd> <dt>

<span data-ttu-id="d2738-206"><span id="DontShowUI"></span><span id="dontshowui"></span><span id="DONTSHOWUI"></span>**DontShowUI**</span><span class="sxs-lookup"><span data-stu-id="d2738-206"><span id="DontShowUI"></span><span id="dontshowui"></span><span id="DONTSHOWUI"></span>**DontShowUI**</span></span>
</dt> <dd>

<span data-ttu-id="d2738-207">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="d2738-207">**REG\_DWORD**</span></span>

<span data-ttu-id="d2738-208">Valeurs possibles :</span><span class="sxs-lookup"><span data-stu-id="d2738-208">Possible values:</span></span><dl> <dd><span data-ttu-id="d2738-209">0-UI (valeur par défaut)</span><span class="sxs-lookup"><span data-stu-id="d2738-209">0 - UI (default)</span></span></dd> <dd><span data-ttu-id="d2738-210">1-aucune interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="d2738-210">1 - No UI</span></span></dd> </dl>

<span data-ttu-id="d2738-211">Activer ou désactiver l’interface utilisateur WER</span><span class="sxs-lookup"><span data-stu-id="d2738-211">Enable or disable the WER UI</span></span>

</dd> <dt>

<span data-ttu-id="d2738-212"><span id="DontSendAdditionalData"></span><span id="dontsendadditionaldata"></span><span id="DONTSENDADDITIONALDATA"></span>**DontSendAdditionalData**</span><span class="sxs-lookup"><span data-stu-id="d2738-212"><span id="DontSendAdditionalData"></span><span id="dontsendadditionaldata"></span><span id="DONTSENDADDITIONALDATA"></span>**DontSendAdditionalData**</span></span>
</dt> <dd>

<span data-ttu-id="d2738-213">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="d2738-213">**REG\_DWORD**</span></span>

<span data-ttu-id="d2738-214">Valeurs possibles :</span><span class="sxs-lookup"><span data-stu-id="d2738-214">Possible values:</span></span><dl> <dd><span data-ttu-id="d2738-215">0-envoyer (par défaut)</span><span class="sxs-lookup"><span data-stu-id="d2738-215">0 - Send (default)</span></span></dd> <dd><span data-ttu-id="d2738-216">1-ne pas envoyer</span><span class="sxs-lookup"><span data-stu-id="d2738-216">1 - Do not send</span></span></dd> </dl>

<span data-ttu-id="d2738-217">Indique s’il faut empêcher l’envoi de données de second niveau</span><span class="sxs-lookup"><span data-stu-id="d2738-217">Whether to prevent sending second-level data</span></span>

</dd> <dt>

<span data-ttu-id="d2738-218"><span id="ExcludedApplications__Application_Name_"></span><span id="excludedapplications__application_name_"></span><span id="EXCLUDEDAPPLICATIONS__APPLICATION_NAME_"></span>**Nom de l' \\ \[ application ExcludedApplications\]**</span><span class="sxs-lookup"><span data-stu-id="d2738-218"><span id="ExcludedApplications__Application_Name_"></span><span id="excludedapplications__application_name_"></span><span id="EXCLUDEDAPPLICATIONS__APPLICATION_NAME_"></span>**ExcludedApplications\\\[Application Name\]**</span></span>
</dt> <dd>

<span data-ttu-id="d2738-219">**SZ de REG \_**</span><span class="sxs-lookup"><span data-stu-id="d2738-219">**REG\_SZ**</span></span>

<span data-ttu-id="d2738-220">Utiliser [ **WerAddExcludedApplication**](/windows/desktop/api/Werapi/nf-werapi-weraddexcludedapplication)</span><span class="sxs-lookup"><span data-stu-id="d2738-220">Use [**WerAddExcludedApplication**](/windows/desktop/api/Werapi/nf-werapi-weraddexcludedapplication)</span></span>

<span data-ttu-id="d2738-221">Liste des applications exclues</span><span class="sxs-lookup"><span data-stu-id="d2738-221">List of excluded applications</span></span>

</dd> <dt>

<span data-ttu-id="d2738-222"><span id="ForceQueue"></span><span id="forcequeue"></span><span id="FORCEQUEUE"></span>**ForceQueue**</span><span class="sxs-lookup"><span data-stu-id="d2738-222"><span id="ForceQueue"></span><span id="forcequeue"></span><span id="FORCEQUEUE"></span>**ForceQueue**</span></span>
</dt> <dd>

<span data-ttu-id="d2738-223">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="d2738-223">**REG\_DWORD**</span></span>

<span data-ttu-id="d2738-224">Valeurs possibles :</span><span class="sxs-lookup"><span data-stu-id="d2738-224">Possible values:</span></span><dl> <dd><span data-ttu-id="d2738-225">0-non (valeur par défaut)</span><span class="sxs-lookup"><span data-stu-id="d2738-225">0 - No (default)</span></span></dd> <dd><span data-ttu-id="d2738-226">1 - Oui</span><span class="sxs-lookup"><span data-stu-id="d2738-226">1 - Yes</span></span></dd> </dl>

<span data-ttu-id="d2738-227">Indique si tous les rapports doivent être envoyés à la file d’attente de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="d2738-227">Whether to send all reports to the user's queue</span></span>

</dd> <dt>

<span data-ttu-id="d2738-228"><span id="LocalDumps_DumpFolder_or_LocalDumps__Application_Name__DumpFolder"></span><span id="localdumps_dumpfolder_or_localdumps__application_name__dumpfolder"></span><span id="LOCALDUMPS_DUMPFOLDER_OR_LOCALDUMPS__APPLICATION_NAME__DUMPFOLDER"></span>**LocalDumps \\ DumpFolder** ou **LocalDumps nom de l' \\ \[ application \] \\ DumpFolder**</span><span class="sxs-lookup"><span data-stu-id="d2738-228"><span id="LocalDumps_DumpFolder_or_LocalDumps__Application_Name__DumpFolder"></span><span id="localdumps_dumpfolder_or_localdumps__application_name__dumpfolder"></span><span id="LOCALDUMPS_DUMPFOLDER_OR_LOCALDUMPS__APPLICATION_NAME__DUMPFOLDER"></span>**LocalDumps\\DumpFolder** or **LocalDumps\\\[Application Name\]\\DumpFolder**</span></span>
</dt> <dd>

<span data-ttu-id="d2738-229">**REG \_ développer \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="d2738-229">**REG\_EXPAND\_SZ**</span></span>

<span data-ttu-id="d2738-230">Chemin d'accès du répertoire.</span><span class="sxs-lookup"><span data-stu-id="d2738-230">The directory path.</span></span> <span data-ttu-id="d2738-231">La valeur par défaut est% LOCALAPPDATA% \\ CrashDumps.</span><span class="sxs-lookup"><span data-stu-id="d2738-231">The default value is %LOCALAPPDATA%\\CrashDumps.</span></span> <span data-ttu-id="d2738-232">Si la valeur par défaut n’est pas utilisée, l’application doit s’assurer que le dossier possède un ACL suffisant.</span><span class="sxs-lookup"><span data-stu-id="d2738-232">If the default is not used, the application must ensure that the folder has a sufficient ACL.</span></span>

<span data-ttu-id="d2738-233">**Windows Vista :** Les valeurs de Registre sous la clé **LocalDumps** ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="d2738-233">**Windows Vista:** The registry values under the **LocalDumps** key are not supported.</span></span> <span data-ttu-id="d2738-234">Notez que ce comportement a changé avec Windows Server 2008 et Windows Vista avec Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="d2738-234">Note that this behavior changed with Windows Server 2008 and Windows Vista with Service Pack 1 (SP1).</span></span>

<span data-ttu-id="d2738-235">Chemin d’accès où les fichiers de vidage doivent être stockés.</span><span class="sxs-lookup"><span data-stu-id="d2738-235">The path where the dump files are to be stored.</span></span>

<span data-ttu-id="d2738-236">Notez que les paramètres par processus remplacent tous les paramètres globaux qui existent pour plus d’informations, consultez [collecte des vidages de User-Mode](collecting-user-mode-dumps.md).</span><span class="sxs-lookup"><span data-stu-id="d2738-236">Note that per-process settings will override any global settings that exist For more information, see [Collecting User-Mode Dumps](collecting-user-mode-dumps.md).</span></span>

<span data-ttu-id="d2738-237">Ce paramètre n’est pas pris en charge dans la ruche de Registre **HKEY \_ Current \_ User** .</span><span class="sxs-lookup"><span data-stu-id="d2738-237">This setting is not supported in the **HKEY\_CURRENT\_USER** registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="d2738-238"><span id="LocalDumps_DumpCount_or_LocalDumps__Application_Name__DumpCount"></span><span id="localdumps_dumpcount_or_localdumps__application_name__dumpcount"></span><span id="LOCALDUMPS_DUMPCOUNT_OR_LOCALDUMPS__APPLICATION_NAME__DUMPCOUNT"></span>**LocalDumps \\ DumpCount** ou **LocalDumps nom de l' \\ \[ application \] \\ DumpCount**</span><span class="sxs-lookup"><span data-stu-id="d2738-238"><span id="LocalDumps_DumpCount_or_LocalDumps__Application_Name__DumpCount"></span><span id="localdumps_dumpcount_or_localdumps__application_name__dumpcount"></span><span id="LOCALDUMPS_DUMPCOUNT_OR_LOCALDUMPS__APPLICATION_NAME__DUMPCOUNT"></span>**LocalDumps\\DumpCount** or **LocalDumps\\\[Application Name\]\\DumpCount**</span></span>
</dt> <dd>

<span data-ttu-id="d2738-239">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="d2738-239">**REG\_DWORD**</span></span>

<span data-ttu-id="d2738-240">Nombre maximal.</span><span class="sxs-lookup"><span data-stu-id="d2738-240">The maximum number.</span></span> <span data-ttu-id="d2738-241">La valeur par défaut est de 10.</span><span class="sxs-lookup"><span data-stu-id="d2738-241">The default is 10.</span></span> <span data-ttu-id="d2738-242">Lorsque la valeur maximale est dépassée, le fichier de vidage le plus ancien dans le dossier sera remplacé par le nouveau fichier de vidage.</span><span class="sxs-lookup"><span data-stu-id="d2738-242">When the maximum value is exceeded, the oldest dump file in the folder will be replaced with the new dump file.</span></span>

<span data-ttu-id="d2738-243">**Windows Vista :** Les valeurs de Registre sous la clé **LocalDumps** ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="d2738-243">**Windows Vista:** The registry values under the **LocalDumps** key are not supported.</span></span> <span data-ttu-id="d2738-244">Notez que ce comportement a changé avec Windows Server 2008 et Windows Vista avec SP1.</span><span class="sxs-lookup"><span data-stu-id="d2738-244">Note that this behavior changed with Windows Server 2008 and Windows Vista with SP1.</span></span>

<span data-ttu-id="d2738-245">Nombre maximal de fichiers de vidage dans le dossier.</span><span class="sxs-lookup"><span data-stu-id="d2738-245">The maximum number of dump files in the folder.</span></span>

<span data-ttu-id="d2738-246">Ce paramètre n’est pas pris en charge dans la ruche de Registre **HKEY \_ Current \_ User** .</span><span class="sxs-lookup"><span data-stu-id="d2738-246">This setting is not supported in the **HKEY\_CURRENT\_USER** registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="d2738-247"><span id="LocalDumps_DumpType_or_LocalDumps__Application_Name__DumpType"></span><span id="localdumps_dumptype_or_localdumps__application_name__dumptype"></span><span id="LOCALDUMPS_DUMPTYPE_OR_LOCALDUMPS__APPLICATION_NAME__DUMPTYPE"></span>**LocalDumps \\ DumpType** ou **LocalDumps nom de l' \\ \[ application \] \\ DumpType**</span><span class="sxs-lookup"><span data-stu-id="d2738-247"><span id="LocalDumps_DumpType_or_LocalDumps__Application_Name__DumpType"></span><span id="localdumps_dumptype_or_localdumps__application_name__dumptype"></span><span id="LOCALDUMPS_DUMPTYPE_OR_LOCALDUMPS__APPLICATION_NAME__DUMPTYPE"></span>**LocalDumps\\DumpType** or **LocalDumps\\\[Application Name\]\\DumpType**</span></span>
</dt> <dd>

<span data-ttu-id="d2738-248">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="d2738-248">**REG\_DWORD**</span></span>

<span data-ttu-id="d2738-249">Valeurs possibles :</span><span class="sxs-lookup"><span data-stu-id="d2738-249">Possible values:</span></span><dl> <dd><span data-ttu-id="d2738-250">0-vidage personnalisé</span><span class="sxs-lookup"><span data-stu-id="d2738-250">0 - Custom dump</span></span></dd> <dd><span data-ttu-id="d2738-251">1-Minidump (par défaut)</span><span class="sxs-lookup"><span data-stu-id="d2738-251">1 - Minidump (default)</span></span></dd> <dd><span data-ttu-id="d2738-252">2-vidage complet</span><span class="sxs-lookup"><span data-stu-id="d2738-252">2 - Full dump</span></span></dd> </dl>

<span data-ttu-id="d2738-253">**Windows Vista :** Les valeurs de Registre sous la clé **LocalDumps** ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="d2738-253">**Windows Vista:** The registry values under the **LocalDumps** key are not supported.</span></span> <span data-ttu-id="d2738-254">Notez que ce comportement a changé avec Windows Server 2008 et Windows Vista avec SP1.</span><span class="sxs-lookup"><span data-stu-id="d2738-254">Note that this behavior changed with Windows Server 2008 and Windows Vista with SP1.</span></span>

<span data-ttu-id="d2738-255">Type de vidage.</span><span class="sxs-lookup"><span data-stu-id="d2738-255">The dump type.</span></span>

<span data-ttu-id="d2738-256">Ce paramètre n’est pas pris en charge dans la ruche de Registre **HKEY \_ Current \_ User** .</span><span class="sxs-lookup"><span data-stu-id="d2738-256">This setting is not supported in the **HKEY\_CURRENT\_USER** registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="d2738-257"><span id="LocalDumps_CustomDumpFlags_or_LocalDumps__Application_Name__CustomDumpFlags"></span><span id="localdumps_customdumpflags_or_localdumps__application_name__customdumpflags"></span><span id="LOCALDUMPS_CUSTOMDUMPFLAGS_OR_LOCALDUMPS__APPLICATION_NAME__CUSTOMDUMPFLAGS"></span>**LocalDumps \\ CustomDumpFlags** ou **LocalDumps nom de l' \\ \[ application \] \\ CustomDumpFlags**</span><span class="sxs-lookup"><span data-stu-id="d2738-257"><span id="LocalDumps_CustomDumpFlags_or_LocalDumps__Application_Name__CustomDumpFlags"></span><span id="localdumps_customdumpflags_or_localdumps__application_name__customdumpflags"></span><span id="LOCALDUMPS_CUSTOMDUMPFLAGS_OR_LOCALDUMPS__APPLICATION_NAME__CUSTOMDUMPFLAGS"></span>**LocalDumps\\CustomDumpFlags** or **LocalDumps\\\[Application Name\]\\CustomDumpFlags**</span></span>
</dt> <dd>

<span data-ttu-id="d2738-258">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="d2738-258">**REG\_DWORD**</span></span>

<span data-ttu-id="d2738-259">Une ou plusieurs valeurs de l’énumération de [**\_ type Minidump**](/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type) .</span><span class="sxs-lookup"><span data-stu-id="d2738-259">One or more values from the [**MINIDUMP\_TYPE**](/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type) enumeration.</span></span> <span data-ttu-id="d2738-260">La valeur par défaut est {**MiniDumpWithDataSegs** \| **MiniDumpWithUnloadedModules** \| **MiniDumpWithProcessThreadData**}.</span><span class="sxs-lookup"><span data-stu-id="d2738-260">The default is {**MiniDumpWithDataSegs**\|**MiniDumpWithUnloadedModules**\|**MiniDumpWithProcessThreadData**}.</span></span>

<span data-ttu-id="d2738-261">**Windows Vista :** Les valeurs de Registre sous la clé **LocalDumps** ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="d2738-261">**Windows Vista:** The registry values under the **LocalDumps** key are not supported.</span></span> <span data-ttu-id="d2738-262">Notez que ce comportement a changé avec Windows Server 2008 et Windows Vista avec SP1.</span><span class="sxs-lookup"><span data-stu-id="d2738-262">Note that this behavior changed with Windows Server 2008 and Windows Vista with SP1.</span></span>

<span data-ttu-id="d2738-263">Options de vidage personnalisées à utiliser.</span><span class="sxs-lookup"><span data-stu-id="d2738-263">The custom dump options to be used.</span></span> <span data-ttu-id="d2738-264">Cette valeur est utilisée uniquement lorsque **DumpType** a la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="d2738-264">This value is used only when **DumpType** is set to 0.</span></span>

<span data-ttu-id="d2738-265">Ce paramètre n’est pas pris en charge dans la ruche de Registre **HKEY \_ Current \_ User** .</span><span class="sxs-lookup"><span data-stu-id="d2738-265">This setting is not supported in the **HKEY\_CURRENT\_USER** registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="d2738-266"><span id="LoggingDisabled"></span><span id="loggingdisabled"></span><span id="LOGGINGDISABLED"></span>**LoggingDisabled**</span><span class="sxs-lookup"><span data-stu-id="d2738-266"><span id="LoggingDisabled"></span><span id="loggingdisabled"></span><span id="LOGGINGDISABLED"></span>**LoggingDisabled**</span></span>
</dt> <dd>

<span data-ttu-id="d2738-267">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="d2738-267">**REG\_DWORD**</span></span>

<span data-ttu-id="d2738-268">Valeurs possibles :</span><span class="sxs-lookup"><span data-stu-id="d2738-268">Possible values:</span></span><dl> <dd><span data-ttu-id="d2738-269">0 – activé (valeur par défaut)</span><span class="sxs-lookup"><span data-stu-id="d2738-269">0–Enabled (default)</span></span></dd> <dd><span data-ttu-id="d2738-270">1 – désactivé</span><span class="sxs-lookup"><span data-stu-id="d2738-270">1–Disabled</span></span></dd> </dl>

<span data-ttu-id="d2738-271">Activer ou désactiver la journalisation</span><span class="sxs-lookup"><span data-stu-id="d2738-271">Enable or disable logging</span></span>

</dd> <dt>

<span data-ttu-id="d2738-272"><span id="MaxArchiveCount"></span><span id="maxarchivecount"></span><span id="MAXARCHIVECOUNT"></span>**MaxArchiveCount**</span><span class="sxs-lookup"><span data-stu-id="d2738-272"><span id="MaxArchiveCount"></span><span id="maxarchivecount"></span><span id="MAXARCHIVECOUNT"></span>**MaxArchiveCount**</span></span>
</dt> <dd>

<span data-ttu-id="d2738-273">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="d2738-273">**REG\_DWORD**</span></span>

<span data-ttu-id="d2738-274">Plage de valeurs possibles : 1 – 5000.</span><span class="sxs-lookup"><span data-stu-id="d2738-274">Range of possible values: 1–5000.</span></span> <span data-ttu-id="d2738-275">La valeur par défaut est 1000.</span><span class="sxs-lookup"><span data-stu-id="d2738-275">The default is 1000.</span></span>

<span data-ttu-id="d2738-276">Taille maximale de l’archive, dans les fichiers</span><span class="sxs-lookup"><span data-stu-id="d2738-276">Maximum size of the archive, in files</span></span>

</dd> <dt>

<span data-ttu-id="d2738-277"><span id="MaxQueueCount"></span><span id="maxqueuecount"></span><span id="MAXQUEUECOUNT"></span>**MaxQueueCount**</span><span class="sxs-lookup"><span data-stu-id="d2738-277"><span id="MaxQueueCount"></span><span id="maxqueuecount"></span><span id="MAXQUEUECOUNT"></span>**MaxQueueCount**</span></span>
</dt> <dd>

<span data-ttu-id="d2738-278">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="d2738-278">**REG\_DWORD**</span></span>

<span data-ttu-id="d2738-279">Plage de valeurs possibles : 1 à 500.</span><span class="sxs-lookup"><span data-stu-id="d2738-279">Range of possible values: 1–500.</span></span> <span data-ttu-id="d2738-280">La valeur par défaut est de 50.</span><span class="sxs-lookup"><span data-stu-id="d2738-280">The default is 50.</span></span>

<span data-ttu-id="d2738-281">Taille maximale de la file d’attente</span><span class="sxs-lookup"><span data-stu-id="d2738-281">Maximum size of the queue</span></span>

</dd> <dt>

<span data-ttu-id="d2738-282"><span id="QueuePesterInterval"></span><span id="queuepesterinterval"></span><span id="QUEUEPESTERINTERVAL"></span>**QueuePesterInterval**</span><span class="sxs-lookup"><span data-stu-id="d2738-282"><span id="QueuePesterInterval"></span><span id="queuepesterinterval"></span><span id="QUEUEPESTERINTERVAL"></span>**QueuePesterInterval**</span></span>
</dt> <dd>

<span data-ttu-id="d2738-283">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="d2738-283">**REG\_DWORD**</span></span>

<span data-ttu-id="d2738-284">Nombre de jours</span><span class="sxs-lookup"><span data-stu-id="d2738-284">Number of days</span></span>

<span data-ttu-id="d2738-285">Intervalle entre les rappels à l’utilisateur pour rechercher des solutions, en jours</span><span class="sxs-lookup"><span data-stu-id="d2738-285">Interval between reminders to the user to check for solutions, in days</span></span>

</dd> <dt>

<span data-ttu-id="d2738-286"><span id="RuntimeExceptionHelperModules___pwszOutOfProcessCallbackDll_name_including_path_"></span><span id="runtimeexceptionhelpermodules___pwszoutofprocesscallbackdll_name_including_path_"></span><span id="RUNTIMEEXCEPTIONHELPERMODULES___PWSZOUTOFPROCESSCALLBACKDLL_NAME_INCLUDING_PATH_"></span>**RuntimeExceptionHelperModules ! \[ nom de pwszOutOfProcessCallbackDll incluant le chemin d’accès\]**</span><span class="sxs-lookup"><span data-stu-id="d2738-286"><span id="RuntimeExceptionHelperModules___pwszOutOfProcessCallbackDll_name_including_path_"></span><span id="runtimeexceptionhelpermodules___pwszoutofprocesscallbackdll_name_including_path_"></span><span id="RUNTIMEEXCEPTIONHELPERMODULES___PWSZOUTOFPROCESSCALLBACKDLL_NAME_INCLUDING_PATH_"></span>**RuntimeExceptionHelperModules!\[ pwszOutOfProcessCallbackDll name including path\]**</span></span>
</dt> <dd>

<span data-ttu-id="d2738-287">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="d2738-287">**REG\_DWORD**</span></span>

<span data-ttu-id="d2738-288">Le contenu de la valeur est ignoré.</span><span class="sxs-lookup"><span data-stu-id="d2738-288">The contents of the value are ignored.</span></span>

<span data-ttu-id="d2738-289">Le nom de la valeur est utilisé pour extraire la valeur pwszOutOfProcessCallbackDll.</span><span class="sxs-lookup"><span data-stu-id="d2738-289">The name of the value is used to fetch the pwszOutOfProcessCallbackDll value.</span></span>

<span data-ttu-id="d2738-290">**Windows server 2008, Windows Vista, Windows server 2003 et Windows XP :** Cette valeur de Registre n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="d2738-290">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This registry value is not supported.</span></span>

</dd> </dl>

## <a name="wer-live-kernel-reports-settings"></a><span data-ttu-id="d2738-291">Paramètres du rapport de noyau en temps réel WER</span><span class="sxs-lookup"><span data-stu-id="d2738-291">WER Live Kernel Reports Settings</span></span>

<span data-ttu-id="d2738-292">Les paramètres des rapports du noyau en direct de WER, décrits ci-après, se trouvent tous deux dans la sous-clé de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="d2738-292">WER's Live Kernel Reports settings, which are described next, are both located under the following registry subkey:</span></span>

-   <span data-ttu-id="d2738-293">**HKEY \_ \_** \\  \\  \\ **Contrôle** CurrentControlSet du système \\  de l’ordinateur local CrashControl</span><span class="sxs-lookup"><span data-stu-id="d2738-293">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Control**\\**CrashControl**</span></span>

## <a name="fulllivekernelreports-subkey"></a><span data-ttu-id="d2738-294">Sous-clé FullLiveKernelReports</span><span class="sxs-lookup"><span data-stu-id="d2738-294">FullLiveKernelReports subkey</span></span>

<dl> <dt>

<span data-ttu-id="d2738-295"><span id="ComponentThrottleThreshold"></span><span id="componentthrottlethreshold"></span><span id="COMPONENTTHROTTLETHRESHOLD"></span>**ComponentThrottleThreshold**</span><span class="sxs-lookup"><span data-stu-id="d2738-295"><span id="ComponentThrottleThreshold"></span><span id="componentthrottlethreshold"></span><span id="COMPONENTTHROTTLETHRESHOLD"></span>**ComponentThrottleThreshold**</span></span>
</dt> <dd>

<span data-ttu-id="d2738-296">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="d2738-296">**REG\_DWORD**</span></span>

<span data-ttu-id="d2738-297">Seuil (en heures) de la fréquence à laquelle un seul composant peut créer un vidage dynamique complet.</span><span class="sxs-lookup"><span data-stu-id="d2738-297">The threshold (in hours) of how often any single component can create a full live dump.</span></span> <span data-ttu-id="d2738-298">Cette valeur doit être supérieure ou égale à **SystemThrottleThreshold**.</span><span class="sxs-lookup"><span data-stu-id="d2738-298">This value must be greater than or equal to **SystemThrottleThreshold**.</span></span> <span data-ttu-id="d2738-299">La définition de la valeur zéro (0) désactivera toutes les limitations temporelles.</span><span class="sxs-lookup"><span data-stu-id="d2738-299">Setting both to zero (0) will disable all time-based throttling.</span></span> <span data-ttu-id="d2738-300">La valeur par défaut est 168 (7 jours).</span><span class="sxs-lookup"><span data-stu-id="d2738-300">The default is 168 (7 days).</span></span>

</dd> <dt>

<span data-ttu-id="d2738-301"><span id="FullLiveReportsMax"></span><span id="fulllivereportsmax"></span><span id="FULLLIVEREPORTSMAX"></span>**FullLiveReportsMax**</span><span class="sxs-lookup"><span data-stu-id="d2738-301"><span id="FullLiveReportsMax"></span><span id="fulllivereportsmax"></span><span id="FULLLIVEREPORTSMAX"></span>**FullLiveReportsMax**</span></span>
</dt> <dd>

<span data-ttu-id="d2738-302">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="d2738-302">**REG\_DWORD**</span></span>

<span data-ttu-id="d2738-303">Nombre maximal de dumps dynamiques complets qui peuvent se trouver sur le disque à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="d2738-303">The maximum number of full live dumps that may be on disk at any given time.</span></span> <span data-ttu-id="d2738-304">La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="d2738-304">The default is 1.</span></span> <span data-ttu-id="d2738-305">Si vous définissez cette valeur sur zéro (0), la fonctionnalité de vidage dynamique est désactivée.</span><span class="sxs-lookup"><span data-stu-id="d2738-305">Setting this value to zero (0) will disable the live dump feature.</span></span>

</dd> <dt>

<span data-ttu-id="d2738-306"><span id="LastFullLiveReport"></span><span id="lastfulllivereport"></span><span id="LASTFULLLIVEREPORT"></span>**LastFullLiveReport**</span><span class="sxs-lookup"><span data-stu-id="d2738-306"><span id="LastFullLiveReport"></span><span id="lastfulllivereport"></span><span id="LASTFULLLIVEREPORT"></span>**LastFullLiveReport**</span></span>
</dt> <dd>

<span data-ttu-id="d2738-307">**\_q QWord**</span><span class="sxs-lookup"><span data-stu-id="d2738-307">**REG\_QWORD**</span></span>

<span data-ttu-id="d2738-308">[SystemTime](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) indiquant la dernière heure de rapport dynamique complète, pour le système ou un ReportType spécifique.</span><span class="sxs-lookup"><span data-stu-id="d2738-308">A [SystemTime](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) indicating the last full live report time, for the system or a specific ReportType.</span></span> <span data-ttu-id="d2738-309">Utilisé pour déterminer si un seuil de stratégie a été respecté.</span><span class="sxs-lookup"><span data-stu-id="d2738-309">This is used to calculate whether a policy threshold has been satisfied.</span></span>

</dd> <dt>

<span data-ttu-id="d2738-310"><span id="SystemThrottleThreshold"></span><span id="systemthrottlethreshold"></span><span id="SYSTEMTHROTTLETHRESHOLD"></span>**SystemThrottleThreshold**</span><span class="sxs-lookup"><span data-stu-id="d2738-310"><span id="SystemThrottleThreshold"></span><span id="systemthrottlethreshold"></span><span id="SYSTEMTHROTTLETHRESHOLD"></span>**SystemThrottleThreshold**</span></span>
</dt> <dd>

<span data-ttu-id="d2738-311">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="d2738-311">**REG\_DWORD**</span></span>

<span data-ttu-id="d2738-312">Seuil (en heures) de la fréquence à laquelle un composant sur le système peut créer un vidage dynamique complet.</span><span class="sxs-lookup"><span data-stu-id="d2738-312">The threshold (in hours) of how often any component on the system can create a full live dump.</span></span> <span data-ttu-id="d2738-313">La valeur par défaut est 120 (5 jours).</span><span class="sxs-lookup"><span data-stu-id="d2738-313">The default is 120 (5 days).</span></span>

</dd> </dl>

## <a name="livekernelreports-subkey"></a><span data-ttu-id="d2738-314">Sous-clé LiveKernelReports</span><span class="sxs-lookup"><span data-stu-id="d2738-314">LiveKernelReports subkey</span></span>

<dl> <dt>

<span data-ttu-id="d2738-315"><span id="LiveKernelReportsPath"></span><span id="livekernelreportspath"></span><span id="LIVEKERNELREPORTSPATH"></span>**LiveKernelReportsPath**</span><span class="sxs-lookup"><span data-stu-id="d2738-315"><span id="LiveKernelReportsPath"></span><span id="livekernelreportspath"></span><span id="LIVEKERNELREPORTSPATH"></span>**LiveKernelReportsPath**</span></span>
</dt> <dd>

<span data-ttu-id="d2738-316">**SZ de REG \_**</span><span class="sxs-lookup"><span data-stu-id="d2738-316">**REG\_SZ**</span></span>


<span data-ttu-id="d2738-317">Emplacement de stockage Redirigé des rapports de noyau en direct.</span><span class="sxs-lookup"><span data-stu-id="d2738-317">The redirected storage location of live kernel reports.</span></span> <span data-ttu-id="d2738-318">L’emplacement par défaut est%systemroot%\LiveKernelReports.</span><span class="sxs-lookup"><span data-stu-id="d2738-318">The default location is %systemroot%\LiveKernelReports.</span></span> <span data-ttu-id="d2738-319">Cette valeur doit être un chemin d’accès valide.</span><span class="sxs-lookup"><span data-stu-id="d2738-319">This value must be a valid path.</span></span> <span data-ttu-id="d2738-320">Le chemin d’accès doit être au format de chemin d’accès NT.</span><span class="sxs-lookup"><span data-stu-id="d2738-320">The path must be in NT path format.</span></span> <span data-ttu-id="d2738-321">Par exemple, \? ? \c : \LiveDumpsFolder.</span><span class="sxs-lookup"><span data-stu-id="d2738-321">For example, \??\C:\LiveDumpsFolder.</span></span>  <span data-ttu-id="d2738-322">Pour plus d’informations sur les formats de chemin d’accès, consultez  [formats de chemin d’accès de fichier sur les systèmes Windows](/dotnet/standard/io/file-path-formats).</span><span class="sxs-lookup"><span data-stu-id="d2738-322">For more information on path formats, see  [File path formats on Windows systems](/dotnet/standard/io/file-path-formats).</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="d2738-323">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d2738-323">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2738-324">Référence WER</span><span class="sxs-lookup"><span data-stu-id="d2738-324">WER Reference</span></span>](wer-reference.md)
</dt> </dl>

 

 
