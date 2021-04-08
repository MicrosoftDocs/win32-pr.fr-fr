---
title: Constantes HTTP_LOGGING_FLAG_ (http. h)
description: Définissez les options de configuration de la journalisation sur l’API du serveur HTTP.
ms.assetid: b6afef7a-5426-4ccd-9785-169e83812c07
topic_type:
- apiref
api_name:
- HTTP_LOGGING_FLAG_LOCAL_TIME_ROLLOVER
- HTTP_LOGGING_FLAG_USE_UTF8_CONVERSION
- HTTP_LOGGING_FLAG_LOG_ERRORS_ONLY
- HTTP_LOGGING_FLAG_LOG_SUCCESS_ONLY
api_location:
- http.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c501fc3ab646ab65fa039a5ff5e7d2dc0578002a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742501"
---
# <a name="http_logging_flag_-constants"></a><span data-ttu-id="feaeb-103">\_ \_ Constantes d’indicateur de JOURNALisation http \_</span><span class="sxs-lookup"><span data-stu-id="feaeb-103">HTTP\_LOGGING\_FLAG\_ Constants</span></span>

<span data-ttu-id="feaeb-104">Les constantes d' **\_ \_ indicateur \_ de journalisation http** définissent les options permettant de configurer la journalisation sur l’API du serveur http.</span><span class="sxs-lookup"><span data-stu-id="feaeb-104">The **HTTP\_LOGGING\_FLAG\_** constants define the options to configure logging on the HTTP Server API.</span></span>

<span data-ttu-id="feaeb-105">Ces constantes sont utilisées dans la structure des [**\_ \_ informations de journalisation http**](/windows/desktop/api/Http/ns-http-http_logging_info) .</span><span class="sxs-lookup"><span data-stu-id="feaeb-105">These constants are used in the [**HTTP\_LOGGING\_INFO**](/windows/desktop/api/Http/ns-http-http_logging_info) structure.</span></span>

<dl> <dt>

<span data-ttu-id="feaeb-106"><span id="HTTP_LOGGING_FLAG_LOCAL_TIME_ROLLOVER"></span><span id="http_logging_flag_local_time_rollover"></span>**\_substitution de \_ l' \_ \_ heure locale \_ de l’indicateur de journalisation http**</span><span class="sxs-lookup"><span data-stu-id="feaeb-106"><span id="HTTP_LOGGING_FLAG_LOCAL_TIME_ROLLOVER"></span><span id="http_logging_flag_local_time_rollover"></span>**HTTP\_LOGGING\_FLAG\_LOCAL\_TIME\_ROLLOVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="feaeb-107">La substitution du fichier journal est basée sur l’heure locale.</span><span class="sxs-lookup"><span data-stu-id="feaeb-107">The log file rollover is based on local time.</span></span> <span data-ttu-id="feaeb-108">Par défaut, les substitutions de fichier journal sont basées sur le temps universel coordonné (UTC).</span><span class="sxs-lookup"><span data-stu-id="feaeb-108">By default, log file rollovers is based on coordinated universal time (UTC).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="feaeb-109"><span id="_HTTP_LOGGING_FLAG_USE_UTF8_CONVERSION"></span><span id="_http_logging_flag_use_utf8_conversion"></span>**Protocole http \_ Indicateur de JOURNALisation \_ \_ utiliser la \_ \_ conversion UTF8**</span><span class="sxs-lookup"><span data-stu-id="feaeb-109"><span id="_HTTP_LOGGING_FLAG_USE_UTF8_CONVERSION"></span><span id="_http_logging_flag_use_utf8_conversion"></span> **HTTP\_LOGGING\_FLAG\_USE\_UTF8\_CONVERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="feaeb-110">Les champs Unicode sont convertis en UTF8 multioctets lors de l’écriture dans les fichiers journaux.</span><span class="sxs-lookup"><span data-stu-id="feaeb-110">The unicode fields are converted to UTF8 multibytes when writting to the log files.</span></span> <span data-ttu-id="feaeb-111">Par défaut, les fichiers journaux sont écrits avec la conversion de la page de codes locale.</span><span class="sxs-lookup"><span data-stu-id="feaeb-111">By default, the log files are written with the local code page conversion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="feaeb-112"><span id="HTTP_LOGGING_FLAG_LOG_ERRORS_ONLY"></span><span id="http_logging_flag_log_errors_only"></span>**indicateur de journalisation HTTP- \_ \_ Erreurs de \_ journal \_ \_ uniquement**</span><span class="sxs-lookup"><span data-stu-id="feaeb-112"><span id="HTTP_LOGGING_FLAG_LOG_ERRORS_ONLY"></span><span id="http_logging_flag_log_errors_only"></span>**HTTP\_LOGGING\_FLAG\_LOG\_ERRORS\_ONLY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="feaeb-113">Les fichiers journaux contiennent uniquement des informations sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="feaeb-113">The log files include error information only.</span></span> <span data-ttu-id="feaeb-114">Par défaut, les réponses d’erreur et de réussite sont journalisées.</span><span class="sxs-lookup"><span data-stu-id="feaeb-114">By default, both error and success responses are logged.</span></span> <span data-ttu-id="feaeb-115">Si l’indicateur de journalisation **http \_ \_ \_ ne consigne pas les \_ Erreurs \_ uniquement** ou si l’indicateur de journalisation http a le **succès du \_ \_ \_ journal \_ \_ uniquement** est défini, les informations d’erreur et de réussite sont consignées.</span><span class="sxs-lookup"><span data-stu-id="feaeb-115">If neither the **HTTP\_LOGGING\_FLAG\_LOG\_ERRORS\_ONLY** or the **HTTP\_LOGGING\_FLAG\_LOG\_SUCCESS\_ONLY** is set, both error and success information is logged.</span></span>

<span data-ttu-id="feaeb-116">Cet indicateur ne peut pas être défini si l’indicateur de **\_ \_ \_ journalisation des échecs de journalisation http \_ \_ uniquement** est également défini.</span><span class="sxs-lookup"><span data-stu-id="feaeb-116">This flag cannot be set if the **HTTP\_LOGGING\_FLAG\_LOG\_SUCCESS\_ONLY** flag is also set.</span></span> <span data-ttu-id="feaeb-117">Ces deux indicateurs s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="feaeb-117">These two flags are mutually exclusive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="feaeb-118"><span id="_HTTP_LOGGING_FLAG_LOG_SUCCESS_ONLY"></span><span id="_http_logging_flag_log_success_only"></span>**Protocole http \_ indicateur de journalisation- \_ \_ réussite du journal \_ \_ uniquement**</span><span class="sxs-lookup"><span data-stu-id="feaeb-118"><span id="_HTTP_LOGGING_FLAG_LOG_SUCCESS_ONLY"></span><span id="_http_logging_flag_log_success_only"></span> **HTTP\_LOGGING\_FLAG\_LOG\_SUCCESS\_ONLY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="feaeb-119">Les fichiers journaux incluent uniquement des informations de réussite.</span><span class="sxs-lookup"><span data-stu-id="feaeb-119">The log files include success information only.</span></span> <span data-ttu-id="feaeb-120">Par défaut, les erreurs et les transactions de réussite sont journalisées.</span><span class="sxs-lookup"><span data-stu-id="feaeb-120">By default, both errors and success transactions are logged.</span></span> <span data-ttu-id="feaeb-121">Si l’indicateur de journalisation **http \_ \_ \_ ne consigne pas les \_ Erreurs \_ uniquement** ou si l’indicateur de journalisation http a le **succès du \_ \_ \_ journal \_ \_ uniquement** est défini, les informations d’erreur et de réussite sont consignées.</span><span class="sxs-lookup"><span data-stu-id="feaeb-121">If neither the **HTTP\_LOGGING\_FLAG\_LOG\_ERRORS\_ONLY** or the **HTTP\_LOGGING\_FLAG\_LOG\_SUCCESS\_ONLY** is set, both error and success information is logged.</span></span>

<span data-ttu-id="feaeb-122">Cet indicateur ne peut pas être défini si l’indicateur de **journalisation http indicateurs d' \_ \_ \_ \_ Erreurs \_ uniquement** est également défini.</span><span class="sxs-lookup"><span data-stu-id="feaeb-122">This flag cannot be set if the **HTTP\_LOGGING\_FLAG\_LOG\_ERRORS\_ONLY** flag is also set.</span></span> <span data-ttu-id="feaeb-123">Ces deux indicateurs s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="feaeb-123">These two flags are mutually exclusive.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="feaeb-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="feaeb-124">Requirements</span></span>



| <span data-ttu-id="feaeb-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="feaeb-125">Requirement</span></span> | <span data-ttu-id="feaeb-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="feaeb-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="feaeb-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="feaeb-127">Minimum supported client</span></span><br/> | <span data-ttu-id="feaeb-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="feaeb-128">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="feaeb-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="feaeb-129">Minimum supported server</span></span><br/> | <span data-ttu-id="feaeb-130">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="feaeb-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="feaeb-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="feaeb-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="feaeb-132"><dt>Http. h</dt></span><span class="sxs-lookup"><span data-stu-id="feaeb-132"><dt>Http.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="feaeb-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="feaeb-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="feaeb-134">Constantes de la version 2,0 de l’API du serveur HTTP</span><span class="sxs-lookup"><span data-stu-id="feaeb-134">HTTP Server API Version 2.0 Constants</span></span>](http-server-api-version-2-0-constants.md)
</dt> <dt>

[<span data-ttu-id="feaeb-135">**\_informations de journalisation http \_**</span><span class="sxs-lookup"><span data-stu-id="feaeb-135">**HTTP\_LOGGING\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_logging_info)
</dt> <dt>

[<span data-ttu-id="feaeb-136">**HttpSetUrlGroupProperty**</span><span class="sxs-lookup"><span data-stu-id="feaeb-136">**HttpSetUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
</dt> <dt>

[<span data-ttu-id="feaeb-137">**HttpSetServerSessionProperty**</span><span class="sxs-lookup"><span data-stu-id="feaeb-137">**HttpSetServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)
</dt> <dt>

[<span data-ttu-id="feaeb-138">**HttpQueryUrlGroupProperty**</span><span class="sxs-lookup"><span data-stu-id="feaeb-138">**HttpQueryUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty)
</dt> <dt>

[<span data-ttu-id="feaeb-139">**HttpQueryServerSessionProperty**</span><span class="sxs-lookup"><span data-stu-id="feaeb-139">**HttpQueryServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)
</dt> </dl>

 

 





