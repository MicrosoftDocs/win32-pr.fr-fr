---
description: La fonction PdhVbOpenLog ouvre le fichier journal spécifié pour la lecture et l’écriture. Cette fonction appelle PdhOpenLog.
ms.assetid: d9b8d98c-64f2-4319-8ab2-67b776143cf7
title: PdhVbOpenLog fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbOpenLog
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 7921585039cab285589f2cdde0f328c033069a87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529115"
---
# <a name="pdhvbopenlog-function"></a><span data-ttu-id="e7541-104">PdhVbOpenLog fonction)</span><span class="sxs-lookup"><span data-stu-id="e7541-104">PdhVbOpenLog function</span></span>

<span data-ttu-id="e7541-105">La fonction **PdhVbOpenLog** ouvre le fichier journal spécifié pour la lecture et l’écriture.</span><span class="sxs-lookup"><span data-stu-id="e7541-105">The **PdhVbOpenLog** function opens the specified log file for reading and writing.</span></span> <span data-ttu-id="e7541-106">Cette fonction appelle [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga).</span><span class="sxs-lookup"><span data-stu-id="e7541-106">This function calls [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e7541-107">La fonction décrite dans cette rubrique peut être modifiée ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="e7541-107">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="e7541-108">Au lieu de cela, Microsoft vous recommande d’utiliser les fonctions décrites dans [fonctions des compteurs de performances](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="e7541-108">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="e7541-109">Fonction PdhVbOpenLog ( \_ ByVal SzLogFileName en tant que LPCTSTR, \_ ByVal DWACCESSFLAGS comme DWORD, \_ BYVAL lpdwLogType comme LPDWORD, \_ ByVal hQuery comme PDH \_ HQUERY, \_ ByVal DwMaxSize comme DWORD, \_ ByVal SZUSERCAPTION comme LPCSTR, \_ ByRef phLog comme PDH \_ HLOG \_ ) comme DWORD</span><span class="sxs-lookup"><span data-stu-id="e7541-109">Function PdhVbOpenLog( \_ ByVal szLogFileName As LPCTSTR, \_ ByVal dwAccessFlags As DWORD, \_ ByVal lpdwLogType As LPDWORD, \_ ByVal hQuery As PDH\_HQUERY, \_ ByVal dwMaxSize As DWORD, \_ ByVal szUserCaption As LPCSTR, \_ ByRef phLog As PDH\_HLOG \_ ) As DWORD</span></span>

## <a name="parameters"></a><span data-ttu-id="e7541-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e7541-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7541-111">*szLogFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e7541-111">*szLogFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7541-112">Pointeur vers une chaîne qui spécifie le nom du fichier journal à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="e7541-112">Pointer to a string that specifies the name of the log file to be opened.</span></span>

<span data-ttu-id="e7541-113">Si le fichier journal contient des données SQL, le format du nom du fichier journal est **SQL :**_DataSourceName_*_!_* _Nom_fichier_journal_.</span><span class="sxs-lookup"><span data-stu-id="e7541-113">If the log file contains SQL data, the format of the name of the log file is **SQL:**_DataSourceName_*_!_*_LogFileName_.</span></span> <span data-ttu-id="e7541-114">Dans ce cas, la valeur du paramètre *lpdwLogType* est le \_ type de journal PDH \_ \_ SQL.</span><span class="sxs-lookup"><span data-stu-id="e7541-114">In this case, the value of the *lpdwLogType* parameter is PDH\_LOG\_TYPE\_SQL.</span></span>

</dd> <dt>

<span data-ttu-id="e7541-115">*dwAccessFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e7541-115">*dwAccessFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7541-116">Type d’accès à spécifier lors de l’ouverture du fichier journal.</span><span class="sxs-lookup"><span data-stu-id="e7541-116">Type of access to be specified when the log file is opened.</span></span> <span data-ttu-id="e7541-117">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="e7541-117">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="e7541-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="e7541-118">Value</span></span>                                                                                                                                                                                   | <span data-ttu-id="e7541-119">Signification</span><span class="sxs-lookup"><span data-stu-id="e7541-119">Meaning</span></span>                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="PDH_LOG_READ_ACCESS"></span><span id="pdh_log_read_access"></span><dl> <span data-ttu-id="e7541-120"><dt>**\_ \_ accès en lecture \_ au Journal PDH**</dt></span><span class="sxs-lookup"><span data-stu-id="e7541-120"><dt>**PDH\_LOG\_READ\_ACCESS**</dt></span></span> </dl>       | <span data-ttu-id="e7541-121">Un fichier journal est ouvert pour une opération de lecture.</span><span class="sxs-lookup"><span data-stu-id="e7541-121">A log file is opened for a read operation.</span></span><br/>            |
| <span id="PDH_LOG_WRITE_ACCESS"></span><span id="pdh_log_write_access"></span><dl> <span data-ttu-id="e7541-122"><dt>**\_accès en \_ écriture \_ au Journal PDH**</dt></span><span class="sxs-lookup"><span data-stu-id="e7541-122"><dt>**PDH\_LOG\_WRITE\_ACCESS**</dt></span></span> </dl>    | <span data-ttu-id="e7541-123">Un nouveau fichier journal est ouvert pour une opération d’écriture.</span><span class="sxs-lookup"><span data-stu-id="e7541-123">A new log file is opened for a write operation.</span></span><br/>       |
| <span id="PDH_LOG_UPDATE_ACCESS"></span><span id="pdh_log_update_access"></span><dl> <span data-ttu-id="e7541-124"><dt>**PDH \_ - \_ accès à la mise à jour des journaux \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e7541-124"><dt>**PDH\_LOG\_UPDATE\_ACCESS**</dt></span></span> </dl> | <span data-ttu-id="e7541-125">Un fichier journal existant est ouvert pour une opération d’écriture.</span><span class="sxs-lookup"><span data-stu-id="e7541-125">An existing log file is opened for a write operation.</span></span><br/> |



 

<span data-ttu-id="e7541-126">La valeur sélectionnée dans le tableau précédent peut être combinée à l’aide de l’opérateur OR avec l’un des indicateurs d’accès Create suivants.</span><span class="sxs-lookup"><span data-stu-id="e7541-126">The value selected from the previous table can be combined using the OR operator with one of the following create access flags.</span></span>



| <span data-ttu-id="e7541-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="e7541-127">Value</span></span>                                                                                                                                                                                   | <span data-ttu-id="e7541-128">Signification</span><span class="sxs-lookup"><span data-stu-id="e7541-128">Meaning</span></span>                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PDH_LOG_CREATE_NEW"></span><span id="pdh_log_create_new"></span><dl> <span data-ttu-id="e7541-129"><dt>**PDH \_ - \_ créer \_ un nouveau journal**</dt></span><span class="sxs-lookup"><span data-stu-id="e7541-129"><dt>**PDH\_LOG\_CREATE\_NEW**</dt></span></span> </dl>          | <span data-ttu-id="e7541-130">Un nouveau fichier journal portant le nom spécifié est créé.</span><span class="sxs-lookup"><span data-stu-id="e7541-130">A new log file with the specified name is created.</span></span><br/>                                                                                                    |
| <span id="PDH_LOG_CREATE_ALWAYS"></span><span id="pdh_log_create_always"></span><dl> <span data-ttu-id="e7541-131"><dt>**PDH \_ - \_ créer \_ toujours le journal**</dt></span><span class="sxs-lookup"><span data-stu-id="e7541-131"><dt>**PDH\_LOG\_CREATE\_ALWAYS**</dt></span></span> </dl> | <span data-ttu-id="e7541-132">Un nouveau fichier journal portant le nom spécifié est créé et tout fichier journal existant portant le même nom est effacé.</span><span class="sxs-lookup"><span data-stu-id="e7541-132">A new log file with the specified name is created and any existing log file with the same name is erased.</span></span><br/>                                             |
| <span id="PDH_LOG_OPEN_EXISTING"></span><span id="pdh_log_open_existing"></span><dl> <span data-ttu-id="e7541-133"><dt>**PDH \_ ouvrir le journal \_ \_ existant**</dt></span><span class="sxs-lookup"><span data-stu-id="e7541-133"><dt>**PDH\_LOG\_OPEN\_EXISTING**</dt></span></span> </dl> | <span data-ttu-id="e7541-134">Un fichier journal existant portant le nom spécifié est ouvert.</span><span class="sxs-lookup"><span data-stu-id="e7541-134">An existing log file with the specified name is opened.</span></span> <span data-ttu-id="e7541-135">Si un fichier journal portant le nom spécifié n’existe pas, il est égal à PDH \_ log \_ Create \_ New.</span><span class="sxs-lookup"><span data-stu-id="e7541-135">If a log file with the specified name does not exist, this is equal to PDH\_LOG\_CREATE\_NEW.</span></span><br/> |
| <span id="PDH_LOG_OPEN_ALWAYS"></span><span id="pdh_log_open_always"></span><dl> <span data-ttu-id="e7541-136"><dt>**PDH \_ ouvrir le journal \_ \_ toujours**</dt></span><span class="sxs-lookup"><span data-stu-id="e7541-136"><dt>**PDH\_LOG\_OPEN\_ALWAYS**</dt></span></span> </dl>       | <span data-ttu-id="e7541-137">Un fichier journal existant portant le nom spécifié est ouvert ou un nouveau fichier journal portant le nom spécifié est créé.</span><span class="sxs-lookup"><span data-stu-id="e7541-137">An existing log file with the specified name is opened or a new log file with the specified name is created.</span></span><br/>                                          |



 

</dd> <dt>

<span data-ttu-id="e7541-138">*lpdwLogType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e7541-138">*lpdwLogType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7541-139">Pointeur vers une variable qui indique le type de fichier journal à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="e7541-139">Pointer to a variable that indicates the type of log file to be opened.</span></span> <span data-ttu-id="e7541-140">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="e7541-140">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="e7541-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="e7541-141">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="e7541-142">Signification</span><span class="sxs-lookup"><span data-stu-id="e7541-142">Meaning</span></span>                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span id="PDH_LOG_TYPE_UNDEFINED"></span><span id="pdh_log_type_undefined"></span><dl> <span data-ttu-id="e7541-143"><dt>**\_type de journal PDH \_ \_ non défini**</dt></span><span class="sxs-lookup"><span data-stu-id="e7541-143"><dt>**PDH\_LOG\_TYPE\_UNDEFINED**</dt></span></span> </dl> | <span data-ttu-id="e7541-144">Format de fichier journal non défini.</span><span class="sxs-lookup"><span data-stu-id="e7541-144">Undefined log file format.</span></span><br/>                                                                                   |
| <span id="PDH_LOG_TYPE_CSV"></span><span id="pdh_log_type_csv"></span><dl> <span data-ttu-id="e7541-145"><dt>**\_type de journal PDH \_ \_ CSV**</dt></span><span class="sxs-lookup"><span data-stu-id="e7541-145"><dt>**PDH\_LOG\_TYPE\_CSV**</dt></span></span> </dl>                   | <span data-ttu-id="e7541-146">Fichiers texte contenant des en-têtes de colonnes dans la première ligne et des exemples de données individuelles sur chaque ligne suivante.</span><span class="sxs-lookup"><span data-stu-id="e7541-146">Text files containing column headers in the first line, and individual data samples in each subsequent line.</span></span><br/> |
| <span id="PDH_LOG_TYPE_SQL"></span><span id="pdh_log_type_sql"></span><dl> <span data-ttu-id="e7541-147"><dt>**\_type de journal PDH \_ \_ SQL**</dt></span><span class="sxs-lookup"><span data-stu-id="e7541-147"><dt>**PDH\_LOG\_TYPE\_SQL**</dt></span></span> </dl>                   | <span data-ttu-id="e7541-148">Les données du fichier journal sont en SQL.</span><span class="sxs-lookup"><span data-stu-id="e7541-148">The data in the log file is in SQL.</span></span><br/>                                                                          |
| <span id="PDH_LOG_TYPE_TSV"></span><span id="pdh_log_type_tsv"></span><dl> <span data-ttu-id="e7541-149"><dt>**\_type de journal PDH \_ \_ TSV**</dt></span><span class="sxs-lookup"><span data-stu-id="e7541-149"><dt>**PDH\_LOG\_TYPE\_TSV**</dt></span></span> </dl>                   | <span data-ttu-id="e7541-150">Identique au \_ type de journal PDH \_ \_ CSV.</span><span class="sxs-lookup"><span data-stu-id="e7541-150">Same as PDH\_LOG\_TYPE\_CSV.</span></span><br/>                                                                                 |
| <span id="PDH_LOG_TYPE_BINARY"></span><span id="pdh_log_type_binary"></span><dl> <span data-ttu-id="e7541-151"><dt>**\_type de journal PDH \_ \_ binaire**</dt></span><span class="sxs-lookup"><span data-stu-id="e7541-151"><dt>**PDH\_LOG\_TYPE\_BINARY**</dt></span></span> </dl>          | <span data-ttu-id="e7541-152">Format du fichier journal binaire.</span><span class="sxs-lookup"><span data-stu-id="e7541-152">Binary log file format.</span></span> <span data-ttu-id="e7541-153">Contient des fichiers journaux circulaires.</span><span class="sxs-lookup"><span data-stu-id="e7541-153">Includes circular log files.</span></span><br/>                                                         |
| <span id="PDH_LOG_TYPE_PERFMON"></span><span id="pdh_log_type_perfmon"></span><dl> <span data-ttu-id="e7541-154"><dt>**\_type de journal PDH \_ \_ Perfmon**</dt></span><span class="sxs-lookup"><span data-stu-id="e7541-154"><dt>**PDH\_LOG\_TYPE\_PERFMON**</dt></span></span> </dl>       | <span data-ttu-id="e7541-155">Format du fichier journal Perfmon.</span><span class="sxs-lookup"><span data-stu-id="e7541-155">Perfmon log file format.</span></span><br/>                                                                                     |



 

</dd> <dt>

<span data-ttu-id="e7541-156">*hQuery* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e7541-156">*hQuery* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7541-157">Handle de requête.</span><span class="sxs-lookup"><span data-stu-id="e7541-157">Query handle.</span></span> <span data-ttu-id="e7541-158">Ce descripteur est retourné par la fonction [**PdhVbOpenQuery**](pdhvbopenquery.md) .</span><span class="sxs-lookup"><span data-stu-id="e7541-158">This handle is returned by the [**PdhVbOpenQuery**](pdhvbopenquery.md) function.</span></span>

<span data-ttu-id="e7541-159">Ce paramètre peut avoir la **valeur null** si le fichier journal doit être ouvert en lecture.</span><span class="sxs-lookup"><span data-stu-id="e7541-159">This parameter can be **NULL** if the log file is to be opened for reading.</span></span>

</dd> <dt>

<span data-ttu-id="e7541-160">*dwMaxSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e7541-160">*dwMaxSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7541-161">Taille maximale du fichier journal, en octets.</span><span class="sxs-lookup"><span data-stu-id="e7541-161">Maximum size of the log file, in bytes.</span></span> <span data-ttu-id="e7541-162">Cette valeur est utilisée uniquement si le fichier journal est un fichier journal de taille limitée ou circulaire.</span><span class="sxs-lookup"><span data-stu-id="e7541-162">This value is used only if the log file is a limited-size or circular log file.</span></span>

</dd> <dt>

<span data-ttu-id="e7541-163">*szUserCaption* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e7541-163">*szUserCaption* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7541-164">Pointeur vers une chaîne qui spécifie la légende définie par l’utilisateur du fichier journal.</span><span class="sxs-lookup"><span data-stu-id="e7541-164">Pointer to a string that specifies the user-defined caption of the log file.</span></span> <span data-ttu-id="e7541-165">Une légende de fichier journal décrit généralement le contenu du fichier journal.</span><span class="sxs-lookup"><span data-stu-id="e7541-165">A log file caption generally describes the contents of the log file.</span></span> <span data-ttu-id="e7541-166">Lorsqu’un fichier journal existant est ouvert, la valeur de ce paramètre est ignorée.</span><span class="sxs-lookup"><span data-stu-id="e7541-166">When an existing log file is opened, the value of this parameter is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="e7541-167">*phLog* \[ in, Ref\]</span><span class="sxs-lookup"><span data-stu-id="e7541-167">*phLog* \[in, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="e7541-168">Pointeur vers une mémoire tampon qui reçoit un handle vers le fichier journal ouvert.</span><span class="sxs-lookup"><span data-stu-id="e7541-168">Pointer to a buffer that receives a handle to the opened log file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7541-169">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e7541-169">Return value</span></span>

<span data-ttu-id="e7541-170">Si la fonction est réussie, elle retourne 0.</span><span class="sxs-lookup"><span data-stu-id="e7541-170">If the function succeeds, it returns 0.</span></span>

<span data-ttu-id="e7541-171">Si la fonction échoue, la valeur de retour est un [code d’erreur système](/windows/desktop/Debug/system-error-codes) ou un [code d’erreur PDH](pdh-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="e7541-171">If the function fails, the return value is a [system error code](/windows/desktop/Debug/system-error-codes) or a [PDH error code](pdh-error-codes.md).</span></span> <span data-ttu-id="e7541-172">Les valeurs possibles sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="e7541-172">The following are possible values.</span></span>



| <span data-ttu-id="e7541-173">Code de retour</span><span class="sxs-lookup"><span data-stu-id="e7541-173">Return code</span></span>                                                                                                | <span data-ttu-id="e7541-174">Description</span><span class="sxs-lookup"><span data-stu-id="e7541-174">Description</span></span>                                                                                            |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e7541-175"><dt>**\_mémoire tampon PDH insuffisante \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e7541-175"><dt>**PDH\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl>   | <span data-ttu-id="e7541-176">Les données demandées sont supérieures à la mémoire tampon fournie.</span><span class="sxs-lookup"><span data-stu-id="e7541-176">The requested data is larger than the buffer supplied.</span></span> <span data-ttu-id="e7541-177">Impossible de retourner les données demandées.</span><span class="sxs-lookup"><span data-stu-id="e7541-177">Unable to return the requested data.</span></span><br/> |
| <dl> <span data-ttu-id="e7541-178"><dt>**PDH \_ argument non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e7541-178"><dt>**PDH\_INVALID\_ARGUMENT**</dt></span></span> </dl>      | <span data-ttu-id="e7541-179">Une ou plusieurs des mémoires tampons de chaîne n’ont pas la taille correcte.</span><span class="sxs-lookup"><span data-stu-id="e7541-179">One or more of the string buffers is not the correct size.</span></span><br/>                                  |
| <dl> <span data-ttu-id="e7541-180"><dt>**\_handle PDH non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e7541-180"><dt>**PDH\_INVALID\_HANDLE**</dt></span></span> </dl>        | <span data-ttu-id="e7541-181">Le descripteur n’est pas un objet PDH valide.</span><span class="sxs-lookup"><span data-stu-id="e7541-181">The handle is not a valid PDH object.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="e7541-182"><dt>**\_erreur d' \_ ouverture du fichier journal \_ PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e7541-182"><dt>**PDH\_LOG\_FILE\_OPEN\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="e7541-183">Impossible d’ouvrir le fichier journal spécifié.</span><span class="sxs-lookup"><span data-stu-id="e7541-183">Unable to open the specified log file.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="e7541-184"><dt>**\_fichier PDH \_ \_ introuvable**</dt></span><span class="sxs-lookup"><span data-stu-id="e7541-184"><dt>**PDH\_FILE\_NOT\_FOUND**</dt></span></span> </dl>       | <span data-ttu-id="e7541-185">Impossible de trouver le fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="e7541-185">Unable to find the specified file.</span></span><br/>                                                          |



 

## <a name="remarks"></a><span data-ttu-id="e7541-186">Notes</span><span class="sxs-lookup"><span data-stu-id="e7541-186">Remarks</span></span>

<span data-ttu-id="e7541-187">Lorsque vous utilisez cette fonction pour écrire des données de performances dans un fichier journal, vous devez d’abord ouvrir une requête à l’aide de [**PdhVbOpenQuery**](pdhvbopenquery.md).</span><span class="sxs-lookup"><span data-stu-id="e7541-187">When using this function to write performance data to a log file, a query must first be opened using [**PdhVbOpenQuery**](pdhvbopenquery.md).</span></span>

<span data-ttu-id="e7541-188">Il doit y avoir une requête actuellement ouverte et les compteurs souhaités doivent y être ajoutés avant que cette fonction soit appelée.</span><span class="sxs-lookup"><span data-stu-id="e7541-188">There must be a currently opened query, and the desired counters must be added to it, before this function is called.</span></span>

<span data-ttu-id="e7541-189">Notez que les fichiers journaux au format Perfmon ne peuvent être ouverts que pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="e7541-189">Note that log files in the Perfmon format can only be opened for reading.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7541-190">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e7541-190">Requirements</span></span>



| <span data-ttu-id="e7541-191">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e7541-191">Requirement</span></span> | <span data-ttu-id="e7541-192">Valeur</span><span class="sxs-lookup"><span data-stu-id="e7541-192">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e7541-193">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7541-193">Minimum supported client</span></span><br/> | <span data-ttu-id="e7541-194">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e7541-194">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e7541-195">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7541-195">Minimum supported server</span></span><br/> | <span data-ttu-id="e7541-196">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e7541-196">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e7541-197">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e7541-197">Library</span></span><br/>                  | <dl> <span data-ttu-id="e7541-198"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e7541-198"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="e7541-199">DLL</span><span class="sxs-lookup"><span data-stu-id="e7541-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7541-200"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7541-200"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7541-201">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7541-201">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7541-202">**PdhOpenLog**</span><span class="sxs-lookup"><span data-stu-id="e7541-202">**PdhOpenLog**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga)
</dt> <dt>

[<span data-ttu-id="e7541-203">**PdhVbGetLogFileSize**</span><span class="sxs-lookup"><span data-stu-id="e7541-203">**PdhVbGetLogFileSize**</span></span>](pdhvbgetlogfilesize.md)
</dt> <dt>

[<span data-ttu-id="e7541-204">**PdhVbUpdateLog**</span><span class="sxs-lookup"><span data-stu-id="e7541-204">**PdhVbUpdateLog**</span></span>](pdhvbupdatelog.md)
</dt> </dl>

 

