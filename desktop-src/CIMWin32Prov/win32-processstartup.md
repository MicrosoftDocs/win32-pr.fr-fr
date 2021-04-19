---
description: La \_ classe WMI ProcessStartup abstraite Win32 représente la configuration de démarrage d’un processus basé sur Windows.
ms.assetid: 78508404-cab2-42fb-a0ed-0e6e7d21408c
ms.tgt_platform: multiple
title: Classe Win32_ProcessStartup
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ProcessStartup
- Win32_ProcessStartup.CreateFlags
- Win32_ProcessStartup.EnvironmentVariables
- Win32_ProcessStartup.ErrorMode
- Win32_ProcessStartup.FillAttribute
- Win32_ProcessStartup.PriorityClass
- Win32_ProcessStartup.ShowWindow
- Win32_ProcessStartup.Title
- Win32_ProcessStartup.WinstationDesktop
- Win32_ProcessStartup.X
- Win32_ProcessStartup.XCountChars
- Win32_ProcessStartup.XSize
- Win32_ProcessStartup.Y
- Win32_ProcessStartup.YCountChars
- Win32_ProcessStartup.YSize
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b0be949b106c1fa88b37e0c7764dbddb0546ded7
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106526716"
---
# <a name="win32_processstartup-class"></a><span data-ttu-id="3c3cc-103">\_Classe ProcessStartup Win32</span><span class="sxs-lookup"><span data-stu-id="3c3cc-103">Win32\_ProcessStartup class</span></span>

<span data-ttu-id="3c3cc-104">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ ProcessStartup** abstraite Win32 représente la configuration de démarrage d’un processus basé sur Windows.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-104">The **Win32\_ProcessStartup** abstract [WMI class](../wmisdk/retrieving-a-class.md) represents the startup configuration of a Windows-based process.</span></span> <span data-ttu-id="3c3cc-105">La classe est définie comme une définition de type de méthode, ce qui signifie qu’elle est utilisée uniquement pour passer des informations à la méthode [**Create**](create-method-in-class-win32-process.md) de la classe de [**\_ processus Win32**](win32-process.md) .</span><span class="sxs-lookup"><span data-stu-id="3c3cc-105">The class is defined as a method type definition, which means that it is only used for passing information to the [**Create**](create-method-in-class-win32-process.md) method of the [**Win32\_Process**](win32-process.md) class.</span></span>

<span data-ttu-id="3c3cc-106">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c3cc-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3c3cc-107">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C4DB-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_ProcessStartup : Win32_MethodParameterClass
{
  uint32 CreateFlags;
  string EnvironmentVariables[];
  uint16 ErrorMode = 1;
  uint32 FillAttribute;
  uint32 PriorityClass;
  uint16 ShowWindow;
  string Title;
  string WinstationDesktop;
  uint32 X;
  uint32 XCountChars;
  uint32 XSize;
  uint32 Y;
  uint32 YCountChars;
  uint32 YSize;
};
```

## <a name="members"></a><span data-ttu-id="3c3cc-108">Membres</span><span class="sxs-lookup"><span data-stu-id="3c3cc-108">Members</span></span>

<span data-ttu-id="3c3cc-109">La classe **Win32 \_ ProcessStartup** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3c3cc-109">The **Win32\_ProcessStartup** class has these types of members:</span></span>

-   [<span data-ttu-id="3c3cc-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3c3cc-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3c3cc-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3c3cc-111">Properties</span></span>

<span data-ttu-id="3c3cc-112">La classe **Win32 \_ ProcessStartup** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-112">The **Win32\_ProcessStartup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3c3cc-113">**CreateFlags**</span><span class="sxs-lookup"><span data-stu-id="3c3cc-113">**CreateFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c3cc-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3c3cc-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3c3cc-115">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3c3cc-115">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3c3cc-116">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Process and thread Functions \| [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) \| dwCreationFlags »)</span><span class="sxs-lookup"><span data-stu-id="3c3cc-116">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Functions\|[**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)\|dwCreationFlags")</span></span>
</dt> </dl>

<span data-ttu-id="3c3cc-117">Valeurs supplémentaires qui contrôlent la classe de priorité et la création du processus.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-117">Additional values that control the priority class and the creation of the process.</span></span> <span data-ttu-id="3c3cc-118">Les valeurs de création suivantes peuvent être spécifiées dans n’importe quelle combinaison, sauf indication contraire.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-118">The following creation values can be specified in any combination, except as noted.</span></span>

<dt>

<span id="Debug_Process"></span><span id="debug_process"></span><span id="DEBUG_PROCESS"></span>

<span data-ttu-id="3c3cc-119"><span id="Debug_Process"></span><span id="debug_process"></span><span id="DEBUG_PROCESS"></span>**Débogage \_ Processus** (1)</span><span class="sxs-lookup"><span data-stu-id="3c3cc-119"><span id="Debug_Process"></span><span id="debug_process"></span><span id="DEBUG_PROCESS"></span>**Debug\_Process** (1)</span></span>


</dt> <dd>

<span data-ttu-id="3c3cc-120">Si cet indicateur est défini, le processus appelant est traité comme un débogueur et le nouveau processus est en cours de débogage.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-120">If this flag is set, the calling process is treated as a debugger, and the new process is being debugged.</span></span> <span data-ttu-id="3c3cc-121">Le système notifie le débogueur de tous les événements de débogage qui se produisent dans le processus en cours de débogage.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-121">The system notifies the debugger of all debug events that occur in the process being debugged.</span></span>

</dd> <dt>

<span id="Debug_Only_This_Process"></span><span id="debug_only_this_process"></span><span id="DEBUG_ONLY_THIS_PROCESS"></span>

<span data-ttu-id="3c3cc-122"><span id="Debug_Only_This_Process"></span><span id="debug_only_this_process"></span><span id="DEBUG_ONLY_THIS_PROCESS"></span>**Débogage \_ Uniquement \_ ce \_ processus** (2)</span><span class="sxs-lookup"><span data-stu-id="3c3cc-122"><span id="Debug_Only_This_Process"></span><span id="debug_only_this_process"></span><span id="DEBUG_ONLY_THIS_PROCESS"></span>**Debug\_Only\_This\_Process** (2)</span></span>


</dt> <dd>

<span data-ttu-id="3c3cc-123">Si cet indicateur n’est pas défini et que le processus appelant est en cours de débogage, le nouveau processus devient un autre processus en cours de débogage.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-123">If this flag is not set and the calling process is being debugged, the new process becomes another process being debugged.</span></span> <span data-ttu-id="3c3cc-124">Si le processus appelant n’est pas un processus de débogage, aucune action relative au débogage ne se produit.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-124">If the calling process is not a process of being debugged, no debugging-related actions occur.</span></span>

</dd> <dt>

<span id="Create_Suspended"></span><span id="create_suspended"></span><span id="CREATE_SUSPENDED"></span>

<span data-ttu-id="3c3cc-125"><span id="Create_Suspended"></span><span id="create_suspended"></span><span id="CREATE_SUSPENDED"></span>**Créer \_ Suspendu** (4)</span><span class="sxs-lookup"><span data-stu-id="3c3cc-125"><span id="Create_Suspended"></span><span id="create_suspended"></span><span id="CREATE_SUSPENDED"></span>**Create\_Suspended** (4)</span></span>


</dt> <dd>

<span data-ttu-id="3c3cc-126">Le thread principal du nouveau processus est créé dans un état suspendu et ne s’exécute pas tant que la méthode [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) n’est pas appelée.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-126">The primary thread of the new process is created in a suspended state and does not run until the [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) method is called.</span></span>

</dd> <dt>

<span id="Detached_Process"></span><span id="detached_process"></span><span id="DETACHED_PROCESS"></span>

<span data-ttu-id="3c3cc-127"><span id="Detached_Process"></span><span id="detached_process"></span><span id="DETACHED_PROCESS"></span>**Détaché \_ Processus** (8)</span><span class="sxs-lookup"><span data-stu-id="3c3cc-127"><span id="Detached_Process"></span><span id="detached_process"></span><span id="DETACHED_PROCESS"></span>**Detached\_Process** (8)</span></span>


</dt> <dd>

<span data-ttu-id="3c3cc-128">Pour les processus de console, le nouveau processus n’a pas accès à la console du processus parent.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-128">For console processes, the new process does not have access to the console of the parent process.</span></span> <span data-ttu-id="3c3cc-129">Cet indicateur ne peut pas être utilisé si l’indicateur **créer \_ un nouvel ensemble de \_ console** est défini.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-129">This flag cannot be used if the **Create\_New\_Console** flag is set.</span></span>

</dd> <dt>

<span id="Create_New_Console"></span><span id="create_new_console"></span><span id="CREATE_NEW_CONSOLE"></span>

<span data-ttu-id="3c3cc-130"><span id="Create_New_Console"></span><span id="create_new_console"></span><span id="CREATE_NEW_CONSOLE"></span>**Créer \_ Nouvelle \_ console** (16)</span><span class="sxs-lookup"><span data-stu-id="3c3cc-130"><span id="Create_New_Console"></span><span id="create_new_console"></span><span id="CREATE_NEW_CONSOLE"></span>**Create\_New\_Console** (16)</span></span>


</dt> <dd>

<span data-ttu-id="3c3cc-131">Ce nouveau processus a une nouvelle console, au lieu d’hériter de la console parente.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-131">This new process has a new console, instead of inheriting the parent console.</span></span> <span data-ttu-id="3c3cc-132">Cet indicateur ne peut pas être utilisé avec l’indicateur de **\_ processus détaché** .</span><span class="sxs-lookup"><span data-stu-id="3c3cc-132">This flag cannot be used with the **Detached\_Process** flag.</span></span>

</dd> <dt>

<span id="Create_New_Process_Group"></span><span id="create_new_process_group"></span><span id="CREATE_NEW_PROCESS_GROUP"></span>

<span data-ttu-id="3c3cc-133"><span id="Create_New_Process_Group"></span><span id="create_new_process_group"></span><span id="CREATE_NEW_PROCESS_GROUP"></span>**Créer \_ Nouveau \_ \_ groupe de processus** (512)</span><span class="sxs-lookup"><span data-stu-id="3c3cc-133"><span id="Create_New_Process_Group"></span><span id="create_new_process_group"></span><span id="CREATE_NEW_PROCESS_GROUP"></span>**Create\_New\_Process\_Group** (512)</span></span>


</dt> <dd>

<span data-ttu-id="3c3cc-134">Ce nouveau processus est le processus racine d’un nouveau groupe de processus.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-134">This new process is the root process of a new process group.</span></span> <span data-ttu-id="3c3cc-135">Le groupe de processus comprend tous les processus qui sont des descendants de ce processus racine.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-135">The process group includes all of the processes that are descendants of this root process.</span></span> <span data-ttu-id="3c3cc-136">L’identificateur de processus du nouveau groupe de processus est le même que celui qui est retourné dans la propriété **ProcessID** de la classe de [**\_ processus Win32**](win32-process.md) .</span><span class="sxs-lookup"><span data-stu-id="3c3cc-136">The process identifier of the new process group is the same as the process identifier that is returned in the **ProcessID** property of the [**Win32\_Process**](win32-process.md) class.</span></span> <span data-ttu-id="3c3cc-137">Les groupes de processus sont utilisés par la méthode [**GenerateConsoleCtrlEvent**](/windows/console/generateconsolectrlevent) pour permettre l’envoi d’un signal Ctrl + C ou d’un signal CTRL + ATTN à un groupe de processus de console.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-137">Process groups are used by the [**GenerateConsoleCtrlEvent**](/windows/console/generateconsolectrlevent) method to enable the sending of either a CTRL+C signal or a CTRL+BREAK signal to a group of console processes.</span></span>

</dd> <dt>

<span id="Create_Unicode_Environment"></span><span id="create_unicode_environment"></span><span id="CREATE_UNICODE_ENVIRONMENT"></span>

<span data-ttu-id="3c3cc-138"><span id="Create_Unicode_Environment"></span><span id="create_unicode_environment"></span><span id="CREATE_UNICODE_ENVIRONMENT"></span>**Créer \_ \_Environnement Unicode** (1024)</span><span class="sxs-lookup"><span data-stu-id="3c3cc-138"><span id="Create_Unicode_Environment"></span><span id="create_unicode_environment"></span><span id="CREATE_UNICODE_ENVIRONMENT"></span>**Create\_Unicode\_Environment** (1024)</span></span>


</dt> <dd>

<span data-ttu-id="3c3cc-139">Les paramètres d’environnement listés dans la propriété **EnvironmentVariables** utilisent des caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-139">The environment settings listed in the **EnvironmentVariables** property use Unicode characters.</span></span> <span data-ttu-id="3c3cc-140">Si cet indicateur n’est pas défini, le bloc d’environnement utilise des caractères ANSI.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-140">If this flag is not set, the environment block uses ANSI characters.</span></span>

</dd> <dt>

<span id="Create_Default_Error_Mode"></span><span id="create_default_error_mode"></span><span id="CREATE_DEFAULT_ERROR_MODE"></span>

<span data-ttu-id="3c3cc-141"><span id="Create_Default_Error_Mode"></span><span id="create_default_error_mode"></span><span id="CREATE_DEFAULT_ERROR_MODE"></span>**Créer \_ \_ \_ Mode d’erreur par défaut** (67108864)</span><span class="sxs-lookup"><span data-stu-id="3c3cc-141"><span id="Create_Default_Error_Mode"></span><span id="create_default_error_mode"></span><span id="CREATE_DEFAULT_ERROR_MODE"></span>**Create\_Default\_Error\_Mode** (67108864)</span></span>


</dt> <dd>

<span data-ttu-id="3c3cc-142">Les processus qui viennent d’être créés reçoivent le mode d’erreur système par défaut du processus appelant au lieu d’hériter du mode d’erreur du processus parent.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-142">Newly created processes are given the system default error mode of the calling process instead of inheriting the error mode of the parent process.</span></span> <span data-ttu-id="3c3cc-143">Cet indicateur est utile pour les applications Shell multithread qui s’exécutent avec des erreurs matérielles désactivées.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-143">This flag is useful for multithreaded shell applications that run with hard errors disabled.</span></span>

</dd> <dt>

<span id="CREATE_BREAKAWAY_FROM_JOB"></span><span id="create_breakaway_from_job"></span>

<span data-ttu-id="3c3cc-144"><span id="CREATE_BREAKAWAY_FROM_JOB"></span><span id="create_breakaway_from_job"></span>**Créer \_ DISSOCIation \_ d’un \_ travail** (16777216)</span><span class="sxs-lookup"><span data-stu-id="3c3cc-144"><span id="CREATE_BREAKAWAY_FROM_JOB"></span><span id="create_breakaway_from_job"></span>**CREATE\_BREAKAWAY\_FROM\_JOB** (16777216)</span></span>


</dt> <dd>

<span data-ttu-id="3c3cc-145">Utilisé pour le processus créé qui ne doit pas être limité par l’objet de traitement.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-145">Used for the created process not to be limited by the job object.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3c3cc-146">**EnvironmentVariables**</span><span class="sxs-lookup"><span data-stu-id="3c3cc-146">**EnvironmentVariables**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c3cc-147">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="3c3cc-147">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3c3cc-148">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3c3cc-148">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3c3cc-149">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| HKEY \_ Current \_ User \\ \\ Environment")</span><span class="sxs-lookup"><span data-stu-id="3c3cc-149">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HKEY\_CURRENT\_USER\\\\Environment")</span></span>
</dt> </dl>

<span data-ttu-id="3c3cc-150">Liste de paramètres pour la configuration d’un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-150">List of settings for the configuration of a computer.</span></span> <span data-ttu-id="3c3cc-151">Les variables d’environnement spécifient des chemins de recherche pour les fichiers, les répertoires de fichiers temporaires, les options spécifiques à l’application et d’autres informations similaires.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-151">Environment variables specify search paths for files, directories for temporary files, application-specific options, and other similar information.</span></span> <span data-ttu-id="3c3cc-152">Le système gère un bloc de paramètres d’environnement pour chaque utilisateur et un pour l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-152">The system maintains a block of environment settings for each user and one for the computer.</span></span> <span data-ttu-id="3c3cc-153">Le bloc environnement système représente les variables d’environnement pour tous les utilisateurs d’un ordinateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-153">The system environment block represents environment variables for all of the users of a specific computer.</span></span> <span data-ttu-id="3c3cc-154">Le bloc environnement d’un utilisateur représente les variables d’environnement gérées par le système pour un utilisateur spécifique, et comprend l’ensemble des variables d’environnement système.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-154">A user's environment block represents the environment variables that the system maintains for a specific user, and includes the set of system environment variables.</span></span> <span data-ttu-id="3c3cc-155">Par défaut, chaque processus reçoit une copie du bloc d’environnement pour son processus parent.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-155">By default, each process receives a copy of the environment block for its parent process.</span></span> <span data-ttu-id="3c3cc-156">En règle générale, il s’agit du bloc d’environnement de l’utilisateur qui a ouvert une session.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-156">Typically, this is the environment block for the user who is logged on.</span></span> <span data-ttu-id="3c3cc-157">Un processus peut spécifier différents blocs d’environnement pour ses processus enfants.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-157">A process can specify different environment blocks for its child processes.</span></span>

</dd> <dt>

<span data-ttu-id="3c3cc-158">**ErrorMode**</span><span class="sxs-lookup"><span data-stu-id="3c3cc-158">**ErrorMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c3cc-159">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3c3cc-159">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3c3cc-160">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3c3cc-160">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3c3cc-161">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Error Functions \| SetErrorMode »)</span><span class="sxs-lookup"><span data-stu-id="3c3cc-161">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Error Functions\|SetErrorMode")</span></span>
</dt> </dl>

<span data-ttu-id="3c3cc-162">Sur certains processeurs non x86, les références de mémoire mal alignées provoquent une exception d’erreur d’alignement.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-162">On some non-x86 processors, misaligned memory references cause an alignment fault exception.</span></span> <span data-ttu-id="3c3cc-163">L’option **aucune \_ faute d’alignement, \_ \_ à l’exception** de l’indicateur, vous permet de contrôler si un système d’exploitation corrige automatiquement ces erreurs d’alignement ou s’il les rend visibles pour une application.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-163">The **No\_Alignment\_Fault\_Except** flag lets you control whether or not an operating system automatically fixes such alignment faults, or makes them visible to an application.</span></span> <span data-ttu-id="3c3cc-164">Sur une plateforme de millions d’instructions par seconde (MIPS), une application doit appeler explicitement [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) avec la faute d’alignement, à l' **\_ \_ \_ exception** de flag pour que le système d’exploitation corrige automatiquement les erreurs d’alignement.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-164">On a millions of instructions per second (MIPS) platform, an application must explicitly call [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) with the **No\_Alignment\_Fault\_Except** flag to have the operating system automatically fix alignment faults.</span></span>

<span data-ttu-id="3c3cc-165">Comment un système d’exploitation traite plusieurs types d’erreurs graves.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-165">How an operating system processes several types of serious errors.</span></span> <span data-ttu-id="3c3cc-166">Vous pouvez spécifier que le système d’exploitation traite les erreurs ou qu’une application puisse recevoir et traiter les erreurs.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-166">You can specify that the operating system process errors, or an application can receive and process errors.</span></span>

<span data-ttu-id="3c3cc-167">Le paramètre par défaut permet au système d’exploitation de rendre visibles les erreurs d’alignement pour une application.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-167">The default setting is for the operating system to make alignment faults visible to an application.</span></span> <span data-ttu-id="3c3cc-168">Étant donné que la plateforme x86 ne rend pas les erreurs d’alignement visibles pour une application, l’absence d’erreur d' **\_ alignement, à l' \_ \_ exception** de Flag, ne fait pas échouer le système d’exploitation, même si l’indicateur n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-168">Because the x86 platform does not make alignment faults visible to an application, the **No\_Alignment\_Fault\_Except** flag does not make the operating system raise an alignment fault error—even if the flag is not set.</span></span> <span data-ttu-id="3c3cc-169">L’État par défaut de [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) consiste à affecter à tous les indicateurs la valeur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="3c3cc-169">The default state for [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) is to set all of the flags to 0 (zero).</span></span>

<dt>



 <span data-ttu-id="3c3cc-170">(1)</span><span class="sxs-lookup"><span data-stu-id="3c3cc-170">(1)</span></span>


</dt> <dd>

<span data-ttu-id="3c3cc-171">Default</span><span class="sxs-lookup"><span data-stu-id="3c3cc-171">Default</span></span>

</dd> <dt>

<span id="Fail_Critical_Errors"></span><span id="fail_critical_errors"></span><span id="FAIL_CRITICAL_ERRORS"></span>

<span data-ttu-id="3c3cc-172"><span id="Fail_Critical_Errors"></span><span id="fail_critical_errors"></span><span id="FAIL_CRITICAL_ERRORS"></span>**Échec \_ \_Erreurs critiques** (2)</span><span class="sxs-lookup"><span data-stu-id="3c3cc-172"><span id="Fail_Critical_Errors"></span><span id="fail_critical_errors"></span><span id="FAIL_CRITICAL_ERRORS"></span>**Fail\_Critical\_Errors** (2)</span></span>


</dt> <dd>

<span data-ttu-id="3c3cc-173">Si cet indicateur est défini, le système d’exploitation n’affiche pas la boîte de message du gestionnaire d’erreurs critiques lorsqu’une telle erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-173">If this flag is set, the operating system does not display the critical error handler message box when such an error occurs.</span></span> <span data-ttu-id="3c3cc-174">Au lieu de cela, le système d’exploitation envoie l’erreur au processus appelant.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-174">Instead, the operating system sends the error to the calling process.</span></span>

</dd> <dt>

<span id="No_Alignment_Fault_Except"></span><span id="no_alignment_fault_except"></span><span id="NO_ALIGNMENT_FAULT_EXCEPT"></span>

<span data-ttu-id="3c3cc-175"><span id="No_Alignment_Fault_Except"></span><span id="no_alignment_fault_except"></span><span id="NO_ALIGNMENT_FAULT_EXCEPT"></span>**Non \_ Erreur d’alignement \_ \_ , sauf** (4)</span><span class="sxs-lookup"><span data-stu-id="3c3cc-175"><span id="No_Alignment_Fault_Except"></span><span id="no_alignment_fault_except"></span><span id="NO_ALIGNMENT_FAULT_EXCEPT"></span>**No\_Alignment\_Fault\_Except** (4)</span></span>


</dt> <dd>

<span data-ttu-id="3c3cc-176">Si cet indicateur est défini, le système d’exploitation corrige automatiquement les erreurs d’alignement de la mémoire et les rend invisibles pour l’application.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-176">If this flag is set, the operating system automatically fixes memory alignment faults and makes them invisible to the application.</span></span> <span data-ttu-id="3c3cc-177">Cela est fait pour les processus d’appel et descendants.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-177">It does this for the calling and descendant processes.</span></span> <span data-ttu-id="3c3cc-178">Cet indicateur s’applique uniquement aux processeurs RISC (Reduced Instruction Set Computing) et n’a aucun effet sur les processeurs x86.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-178">This flag applies to reduced instruction set computing (RISC) only, and has no effect on x86 processors.</span></span>

</dd> <dt>

<span id="No_GP_Fault_Error_Box"></span><span id="no_gp_fault_error_box"></span><span id="NO_GP_FAULT_ERROR_BOX"></span>

<span data-ttu-id="3c3cc-179"><span id="No_GP_Fault_Error_Box"></span><span id="no_gp_fault_error_box"></span><span id="NO_GP_FAULT_ERROR_BOX"></span>**Non \_ \_Boîte de \_ message \_ d’erreur de stratégie de défaut** (8)</span><span class="sxs-lookup"><span data-stu-id="3c3cc-179"><span id="No_GP_Fault_Error_Box"></span><span id="no_gp_fault_error_box"></span><span id="NO_GP_FAULT_ERROR_BOX"></span>**No\_GP\_Fault\_Error\_Box** (8)</span></span>


</dt> <dd>

<span data-ttu-id="3c3cc-180">Si cet indicateur est défini, le système d’exploitation n’affiche pas la boîte de message d’erreur de protection générale lorsqu’une erreur de stratégie de groupe se produit.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-180">If this flag is set, the operating system does not display the general protection (GP) fault message box when a GP error occurs.</span></span> <span data-ttu-id="3c3cc-181">Cet indicateur doit être défini uniquement par les applications de débogage qui gèrent les erreurs de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-181">This flag should only be set by debugging applications that handle GP errors.</span></span>

</dd> <dt>

<span id="No_Open_File_Error_Box"></span><span id="no_open_file_error_box"></span><span id="NO_OPEN_FILE_ERROR_BOX"></span>

<span data-ttu-id="3c3cc-182"><span id="No_Open_File_Error_Box"></span><span id="no_open_file_error_box"></span><span id="NO_OPEN_FILE_ERROR_BOX"></span>**Non \_ \_Boîte de \_ message \_ d’erreur ouvrir le fichier** (16)</span><span class="sxs-lookup"><span data-stu-id="3c3cc-182"><span id="No_Open_File_Error_Box"></span><span id="no_open_file_error_box"></span><span id="NO_OPEN_FILE_ERROR_BOX"></span>**No\_Open\_File\_Error\_Box** (16)</span></span>


</dt> <dd>

<span data-ttu-id="3c3cc-183">Si cet indicateur est défini, le système d’exploitation n’affiche pas de boîte de message lorsqu’il ne parvient pas à trouver un fichier.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-183">If this flag is set, the operating system does not display a message box when it fails to find a file.</span></span> <span data-ttu-id="3c3cc-184">Au lieu de cela, l’erreur est retournée au processus appelant.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-184">Instead, the error is returned to the calling process.</span></span> <span data-ttu-id="3c3cc-185">Cet indicateur est actuellement ignoré.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-185">This flag is currently ignored.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3c3cc-186">**FillAttribute**</span><span class="sxs-lookup"><span data-stu-id="3c3cc-186">**FillAttribute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c3cc-187">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3c3cc-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3c3cc-188">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3c3cc-188">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3c3cc-189">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process and thread structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwFillAttribute")</span><span class="sxs-lookup"><span data-stu-id="3c3cc-189">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|dwFillAttribute")</span></span>
</dt> </dl>

<span data-ttu-id="3c3cc-190">Les couleurs de texte et d’arrière-plan si une nouvelle fenêtre de console est créée dans une application console.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-190">The text and background colors if a new console window is created in a console application.</span></span> <span data-ttu-id="3c3cc-191">Ces valeurs sont ignorées dans les applications d’interface utilisateur graphique (GUI).</span><span class="sxs-lookup"><span data-stu-id="3c3cc-191">These values are ignored in graphical user interface (GUI) applications.</span></span> <span data-ttu-id="3c3cc-192">Pour spécifier les couleurs de premier plan et d’arrière-plan, ajoutez les valeurs ensemble.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-192">To specify both foreground and background colors, add the values together.</span></span> <span data-ttu-id="3c3cc-193">Par exemple, pour avoir le type rouge (4) sur un arrière-plan bleu (16), définissez FillAttribute sur 20.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-193">For example, to have red type (4) on a blue background (16), set the FillAttribute to 20.</span></span>

<dt>

<span data-ttu-id="3c3cc-194">1</span><span class="sxs-lookup"><span data-stu-id="3c3cc-194">1</span></span>
</dt> <dd>

<span data-ttu-id="3c3cc-195">Bleu de premier plan \_</span><span class="sxs-lookup"><span data-stu-id="3c3cc-195">Foreground\_Blue</span></span>

</dd> <dt>

<span data-ttu-id="3c3cc-196">2</span><span class="sxs-lookup"><span data-stu-id="3c3cc-196">2</span></span>
</dt> <dd>

<span data-ttu-id="3c3cc-197">Vert de premier plan \_</span><span class="sxs-lookup"><span data-stu-id="3c3cc-197">Foreground\_Green</span></span>

</dd> <dt>

<span data-ttu-id="3c3cc-198">4</span><span class="sxs-lookup"><span data-stu-id="3c3cc-198">4</span></span>
</dt> <dd>

<span data-ttu-id="3c3cc-199">Premier plan \_ rouge</span><span class="sxs-lookup"><span data-stu-id="3c3cc-199">Foreground\_Red</span></span>

</dd> <dt>

<span data-ttu-id="3c3cc-200">8</span><span class="sxs-lookup"><span data-stu-id="3c3cc-200">8</span></span>
</dt> <dd>

<span data-ttu-id="3c3cc-201">Intensité du premier plan \_</span><span class="sxs-lookup"><span data-stu-id="3c3cc-201">Foreground\_Intensity</span></span>

</dd> <dt>

<span data-ttu-id="3c3cc-202">16</span><span class="sxs-lookup"><span data-stu-id="3c3cc-202">16</span></span>
</dt> <dd>

<span data-ttu-id="3c3cc-203">Arrière-plan \_ bleu</span><span class="sxs-lookup"><span data-stu-id="3c3cc-203">Background\_Blue</span></span>

</dd> <dt>

<span data-ttu-id="3c3cc-204">32</span><span class="sxs-lookup"><span data-stu-id="3c3cc-204">32</span></span>
</dt> <dd>

<span data-ttu-id="3c3cc-205">Arrière-plan \_ vert</span><span class="sxs-lookup"><span data-stu-id="3c3cc-205">Background\_Green</span></span>

</dd> <dt>

<span data-ttu-id="3c3cc-206">64</span><span class="sxs-lookup"><span data-stu-id="3c3cc-206">64</span></span>
</dt> <dd>

<span data-ttu-id="3c3cc-207">Arrière-plan \_ rouge</span><span class="sxs-lookup"><span data-stu-id="3c3cc-207">Background\_Red</span></span>

</dd> <dt>

<span data-ttu-id="3c3cc-208">128</span><span class="sxs-lookup"><span data-stu-id="3c3cc-208">128</span></span>
</dt> <dd>

<span data-ttu-id="3c3cc-209">Intensité de l’arrière-plan \_</span><span class="sxs-lookup"><span data-stu-id="3c3cc-209">Background\_Intensity</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3c3cc-210">**PriorityClass**</span><span class="sxs-lookup"><span data-stu-id="3c3cc-210">**PriorityClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c3cc-211">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3c3cc-211">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3c3cc-212">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3c3cc-212">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3c3cc-213">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Process and thread structures \| [**JOBOBJECT \_ Basic \_ Limit \_ information**](/windows/win32/api/winnt/ns-winnt-jobobject_basic_limit_information) \| PriorityClass »)</span><span class="sxs-lookup"><span data-stu-id="3c3cc-213">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**JOBOBJECT\_BASIC\_LIMIT\_INFORMATION**](/windows/win32/api/winnt/ns-winnt-jobobject_basic_limit_information)\|PriorityClass")</span></span>
</dt> </dl>

<span data-ttu-id="3c3cc-214">Classe de priorité du nouveau processus.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-214">Priority class of the new process.</span></span> <span data-ttu-id="3c3cc-215">Utilisez cette propriété pour déterminer les priorités de planification des threads dans le processus.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-215">Use this property to determine the schedule priorities of the threads in the process.</span></span> <span data-ttu-id="3c3cc-216">Si la propriété est laissée null, la classe Priority est définie par défaut sur normal, à moins que la classe de priorité du processus de création soit inactive ou inférieure à la \_ normale.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-216">If the property is left null, the priority class defaults to Normal—unless the priority class of the creating process is Idle or Below\_Normal.</span></span> <span data-ttu-id="3c3cc-217">Dans ce cas, le processus enfant reçoit la classe de priorité par défaut du processus appelant.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-217">In these cases, the child process receives the default priority class of the calling process.</span></span>

<dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="3c3cc-218"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (32)</span><span class="sxs-lookup"><span data-stu-id="3c3cc-218"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (32)</span></span>


</dt> <dd>

<span data-ttu-id="3c3cc-219">Indique un processus normal sans besoin de planification spécifique.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-219">Indicates a normal process with no special schedule needs.</span></span>

</dd> <dt>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>

<span data-ttu-id="3c3cc-220"><span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Inactif** (64)</span><span class="sxs-lookup"><span data-stu-id="3c3cc-220"><span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Idle** (64)</span></span>


</dt> <dd>

<span data-ttu-id="3c3cc-221">Indique un processus avec des threads qui s’exécutent uniquement lorsque le système est inactif et qui sont précédés par les threads de tout processus s’exécutant dans une classe de priorité plus élevée.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-221">Indicates a process with threads that run only when the system is idle and are preempted by the threads of any process running in a higher priority class.</span></span> <span data-ttu-id="3c3cc-222">Par exemple, un écran de veille.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-222">An example is a screen saver.</span></span> <span data-ttu-id="3c3cc-223">La classe de priorité Idle est héritée par les processus enfants.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-223">The idle priority class is inherited by child processes.</span></span>

</dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="3c3cc-224"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**Élevé** (128)</span><span class="sxs-lookup"><span data-stu-id="3c3cc-224"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**High** (128)</span></span>


</dt> <dd>

<span data-ttu-id="3c3cc-225">Indique un processus qui exécute des tâches critiques à l’heure qui doivent être exécutées immédiatement pour s’exécuter correctement.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-225">Indicates a process that performs time-critical tasks that must be executed immediately to run correctly.</span></span> <span data-ttu-id="3c3cc-226">Les threads d’un processus de classe de priorité élevée prévalent sur les threads de processus de classe de priorité normale ou d’inactivité.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-226">The threads of a high-priority class process preempt the threads of normal-priority or idle-priority class processes.</span></span> <span data-ttu-id="3c3cc-227">C’est le cas, par exemple, de Windows Liste des tâches, qui doit répondre rapidement lorsqu’il est appelé par l’utilisateur, quelle que soit la charge sur le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-227">An example is Windows Task List, which must respond quickly when called by the user, regardless of the load on the operating system.</span></span> <span data-ttu-id="3c3cc-228">Soyez extrêmement vigilant lorsque vous utilisez la classe de priorité élevée, car une application de classe haute priorité basée sur l’UC peut utiliser presque tous les cycles disponibles.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-228">Use extreme care when using the high-priority class, because a high-priority class CPU-bound application can use nearly all of the available cycles.</span></span> <span data-ttu-id="3c3cc-229">Seule une priorité en temps réel anticipe les threads définis à ce niveau.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-229">Only a real-time priority preempts threads set to this level.</span></span>

</dd> <dt>

<span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>

<span data-ttu-id="3c3cc-230"><span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>**Temps réel** (256)</span><span class="sxs-lookup"><span data-stu-id="3c3cc-230"><span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>**Realtime** (256)</span></span>


</dt> <dd>

<span data-ttu-id="3c3cc-231">Indique un processus qui a la priorité la plus élevée possible.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-231">Indicates a process that has the highest possible priority.</span></span> <span data-ttu-id="3c3cc-232">Les threads d’un processus de classe de priorité en temps réel devancent les threads de tous les autres processus, y compris les threads haute priorité et les processus du système d’exploitation qui effectuent des tâches importantes.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-232">The threads of a real-time priority class process preempt the threads of all other processes—including high-priority threads and operating system processes performing important tasks.</span></span> <span data-ttu-id="3c3cc-233">Par exemple, un processus en temps réel qui s’exécute depuis plus d’un intervalle très court peut entraîner le vidage des caches de disque ou l’absence de réponse de la souris.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-233">For example, a real-time process that executes for more than a very brief interval can cause disk caches not to flush, or cause a mouse to be unresponsive.</span></span>

</dd> <dt>

<span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>

<span data-ttu-id="3c3cc-234"><span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>**Ci-dessous \_ Normal** (16384)</span><span class="sxs-lookup"><span data-stu-id="3c3cc-234"><span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>**Below\_Normal** (16384)</span></span>


</dt> <dd>

<span data-ttu-id="3c3cc-235">Indique un processus dont la priorité est supérieure à inactif, mais inférieure à la normale.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-235">Indicates a process that has a priority higher than Idle but lower than Normal.</span></span>

</dd> <dt>

<span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>

<span data-ttu-id="3c3cc-236"><span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>**Ci-dessus \_ Normal** (32768)</span><span class="sxs-lookup"><span data-stu-id="3c3cc-236"><span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>**Above\_Normal** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="3c3cc-237">Indique un processus dont la priorité est supérieure à la normale mais inférieure à la valeur élevée.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-237">Indicates a process that has a priority higher than Normal but lower than High.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3c3cc-238">**ShowWindow**</span><span class="sxs-lookup"><span data-stu-id="3c3cc-238">**ShowWindow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c3cc-239">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3c3cc-239">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3c3cc-240">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3c3cc-240">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3c3cc-241">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process and thread structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| wShowWindow")</span><span class="sxs-lookup"><span data-stu-id="3c3cc-241">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|wShowWindow")</span></span>
</dt> </dl>

<span data-ttu-id="3c3cc-242">Mode d’affichage de la fenêtre pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-242">How the window is displayed to the user.</span></span> <span data-ttu-id="3c3cc-243">Il peut s’agir de l’une des valeurs qui peuvent être spécifiées dans le paramètre *nCmdShow* pour la fonction [ShowWindow](/windows/desktop/api/winuser/nf-winuser-showwindow) .</span><span class="sxs-lookup"><span data-stu-id="3c3cc-243">It can be any of the values that can be specified in the *nCmdShow* parameter for the [ShowWindow](/windows/desktop/api/winuser/nf-winuser-showwindow) function.</span></span>

</dd> <dt>

<span data-ttu-id="3c3cc-244">**Titre**</span><span class="sxs-lookup"><span data-stu-id="3c3cc-244">**Title**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c3cc-245">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3c3cc-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c3cc-246">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3c3cc-246">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3c3cc-247">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process and thread structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| lpTitle")</span><span class="sxs-lookup"><span data-stu-id="3c3cc-247">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|lpTitle")</span></span>
</dt> </dl>

<span data-ttu-id="3c3cc-248">Texte affiché dans la barre de titre lors de la création d’une nouvelle fenêtre de console ; utilisé pour les processus de console.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-248">Text displayed in the title bar when a new console window is created; used for console processes.</span></span> <span data-ttu-id="3c3cc-249">Si la **valeur est null**, le nom du fichier exécutable est utilisé comme titre de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-249">If **NULL**, the name of the executable file is used as the window title.</span></span> <span data-ttu-id="3c3cc-250">Cette propriété doit avoir la **valeur null** pour les processus d’interface utilisateur graphique ou de console qui ne créent pas de nouvelle fenêtre de console.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-250">This property must be **NULL** for GUI or console processes that do not create a new console window.</span></span>

</dd> <dt>

<span data-ttu-id="3c3cc-251">**WinstationDesktop**</span><span class="sxs-lookup"><span data-stu-id="3c3cc-251">**WinstationDesktop**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c3cc-252">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3c3cc-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c3cc-253">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3c3cc-253">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3c3cc-254">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process and thread structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| lpDesktop")</span><span class="sxs-lookup"><span data-stu-id="3c3cc-254">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|lpDesktop")</span></span>
</dt> </dl>

<span data-ttu-id="3c3cc-255">Le nom du bureau ou le nom du bureau et de la station Windows pour le processus.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-255">The name of the desktop or the name of both the desktop and window station for the process.</span></span> <span data-ttu-id="3c3cc-256">Une barre oblique inverse dans la chaîne indique que la chaîne comprend à la fois les noms de station de travail et de station Windows.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-256">A backslash in the string indicates that the string includes both desktop and window station names.</span></span> <span data-ttu-id="3c3cc-257">Si **WinstationDesktop** a la **valeur null**, le nouveau processus hérite du bureau et de la station Windows de son processus parent.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-257">If **WinstationDesktop** is **NULL**, the new process inherits the desktop and window station of its parent process.</span></span> <span data-ttu-id="3c3cc-258">Si **WinstationDesktop** est une chaîne vide, le processus n’hérite pas du bureau et de la station Windows de son processus parent.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-258">If **WinstationDesktop** is an empty string, the process does not inherit the desktop and window station of its parent process.</span></span> <span data-ttu-id="3c3cc-259">Le système détermine si un nouveau bureau et une station Windows doivent être créés.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-259">The system determines if a new desktop and window station must be created.</span></span> <span data-ttu-id="3c3cc-260">Une station Windows est un objet sécurisé qui contient un presse-papiers, un ensemble d’atomes globaux et un groupe d’objets de bureau.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-260">A window station is a secure object that contains a clipboard, a set of global atoms, and a group of desktop objects.</span></span> <span data-ttu-id="3c3cc-261">La station de fenêtre interactive qui est assignée à la session d’ouverture de session de l’utilisateur interactif contient également le clavier, la souris et le périphérique d’affichage.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-261">The interactive window station that is assigned to the logon session of the interactive user also contains the keyboard, mouse, and display device.</span></span> <span data-ttu-id="3c3cc-262">Un bureau est un objet sécurisé contenu dans une station Windows.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-262">A desktop is a secure object contained within a window station.</span></span> <span data-ttu-id="3c3cc-263">Un bureau a une surface d’affichage logique et contient des fenêtres, des menus et des crochets.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-263">A desktop has a logical display surface and contains windows, menus, and hooks.</span></span> <span data-ttu-id="3c3cc-264">Une station Windows peut avoir plusieurs bureaux.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-264">A window station can have multiple desktops.</span></span> <span data-ttu-id="3c3cc-265">Seuls les ordinateurs de bureau de la station Windows Interactive peuvent être visibles et recevoir des entrées utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-265">Only the desktops of the interactive window station can be visible and receive user input.</span></span>

</dd> <dt>

<span data-ttu-id="3c3cc-266">**X**</span><span class="sxs-lookup"><span data-stu-id="3c3cc-266">**X**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c3cc-267">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3c3cc-267">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3c3cc-268">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3c3cc-268">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3c3cc-269">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process and thread structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| DWX")</span><span class="sxs-lookup"><span data-stu-id="3c3cc-269">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|dwX")</span></span>
</dt> </dl>

<span data-ttu-id="3c3cc-270">Décalage X de l’angle supérieur gauche d’une fenêtre si une nouvelle fenêtre est créée, en pixels.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-270">The X offset of the upper left corner of a window if a new window is created—in pixels.</span></span> <span data-ttu-id="3c3cc-271">Les décalages s’affichent dans le coin supérieur gauche de l’écran.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-271">The offsets are from the upper left corner of the screen.</span></span> <span data-ttu-id="3c3cc-272">Pour les processus d’interface utilisateur graphique, la position spécifiée est utilisée la première fois que le nouveau processus appelle [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) pour créer une fenêtre Overlapped si le paramètre *X* de **CreateWindow** est **CW \_ usedefault**.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-272">For GUI processes, the specified position is used the first time the new process calls [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) to create an overlapped window if the *X* parameter of **CreateWindow** is **CW\_USEDEFAULT**.</span></span>

> <span data-ttu-id="3c3cc-273">\[! Remarque X\]</span><span class="sxs-lookup"><span data-stu-id="3c3cc-273">\[!Note  X\]</span></span>  
> <span data-ttu-id="3c3cc-274">et **Y** ne peuvent pas être spécifiés indépendamment.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-274">and **Y** cannot be specified independently.</span></span>

 

</dd> <dt>

<span data-ttu-id="3c3cc-275">**XCountChars**</span><span class="sxs-lookup"><span data-stu-id="3c3cc-275">**XCountChars**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c3cc-276">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3c3cc-276">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3c3cc-277">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3c3cc-277">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3c3cc-278">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process and thread structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| XCountChars")</span><span class="sxs-lookup"><span data-stu-id="3c3cc-278">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|XCountChars")</span></span>
</dt> </dl>

<span data-ttu-id="3c3cc-279">Largeur de la mémoire tampon d’écran dans les colonnes de caractères.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-279">Screen buffer width in character columns.</span></span> <span data-ttu-id="3c3cc-280">Cette propriété est utilisée pour les processus qui créent une fenêtre de console et est ignorée dans les processus GUI.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-280">This property is used for processes that create a console window, and is ignored in GUI processes.</span></span>

> [!Note]  
> <span data-ttu-id="3c3cc-281">**XCountChars** et **YCountChars** ne peuvent pas être spécifiés indépendamment.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-281">**XCountChars** and **YCountChars** cannot be specified independently.</span></span>

 

</dd> <dt>

<span data-ttu-id="3c3cc-282">**XSize**</span><span class="sxs-lookup"><span data-stu-id="3c3cc-282">**XSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c3cc-283">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3c3cc-283">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3c3cc-284">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3c3cc-284">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3c3cc-285">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process and thread structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwXSize")</span><span class="sxs-lookup"><span data-stu-id="3c3cc-285">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|dwXSize")</span></span>
</dt> </dl>

<span data-ttu-id="3c3cc-286">Largeur en pixels d’une fenêtre si une nouvelle fenêtre est créée.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-286">Pixel width of a window if a new window is created.</span></span> <span data-ttu-id="3c3cc-287">Pour les processus GUI, cette méthode est utilisée uniquement la première fois que le nouveau processus appelle [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) pour créer une fenêtre avec chevauchement si le paramètre NWidth de **CreateWindow** est **CW \_ usedefault**.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-287">For GUI processes, this is only used the first time the new process calls [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) to create an overlapped window if the nWidth parameter of **CreateWindow** is **CW\_USEDEFAULT**.</span></span>

> [!Note]  
> <span data-ttu-id="3c3cc-288">**XSIZE** et **YSize** ne peuvent pas être spécifiés indépendamment.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-288">**XSize** and **YSize** cannot be specified independently.</span></span>

 

</dd> <dt>

<span data-ttu-id="3c3cc-289">**O**</span><span class="sxs-lookup"><span data-stu-id="3c3cc-289">**Y**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c3cc-290">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3c3cc-290">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3c3cc-291">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3c3cc-291">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3c3cc-292">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process and thread structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwy")</span><span class="sxs-lookup"><span data-stu-id="3c3cc-292">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|dwY")</span></span>
</dt> </dl>

<span data-ttu-id="3c3cc-293">Décalage de pixel de l’angle supérieur gauche d’une fenêtre si une nouvelle fenêtre est créée.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-293">Pixel offset of the upper-left corner of a window if a new window is created.</span></span> <span data-ttu-id="3c3cc-294">Les décalages proviennent de l’angle supérieur gauche de l’écran.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-294">The offsets are from the upper-left corner of the screen.</span></span> <span data-ttu-id="3c3cc-295">Pour les processus d’interface utilisateur graphique, la position spécifiée est utilisée la première fois que le nouveau processus appelle [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) pour créer une fenêtre Overlapped si le paramètre *y* de **CreateWindow** est **CW \_ usedefault**.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-295">For GUI processes, the specified position is used the first time the new process calls [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) to create an overlapped window if the *y* parameter of **CreateWindow** is **CW\_USEDEFAULT**.</span></span>

> <span data-ttu-id="3c3cc-296">\[! Remarque X\]</span><span class="sxs-lookup"><span data-stu-id="3c3cc-296">\[!Note  X\]</span></span>  
> <span data-ttu-id="3c3cc-297">et **Y** ne peuvent pas être spécifiés indépendamment.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-297">and **Y** cannot be specified independently.</span></span>

 

</dd> <dt>

<span data-ttu-id="3c3cc-298">**YCountChars**</span><span class="sxs-lookup"><span data-stu-id="3c3cc-298">**YCountChars**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c3cc-299">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3c3cc-299">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3c3cc-300">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3c3cc-300">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3c3cc-301">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process and thread structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| YCountChars")</span><span class="sxs-lookup"><span data-stu-id="3c3cc-301">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|YCountChars")</span></span>
</dt> </dl>

<span data-ttu-id="3c3cc-302">Hauteur de la mémoire tampon d’écran dans les lignes de caractères.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-302">Screen buffer height in character rows.</span></span> <span data-ttu-id="3c3cc-303">Cette propriété est utilisée pour les processus qui créent une fenêtre de console, mais elle est ignorée dans les processus GUI.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-303">This property is used for processes that create a console window, but is ignored in GUI processes.</span></span>

> [!Note]  
> <span data-ttu-id="3c3cc-304">**XCountChars** et **YCountChars** ne peuvent pas être spécifiés indépendamment.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-304">**XCountChars** and **YCountChars** cannot be specified independently.</span></span>

 

</dd> <dt>

<span data-ttu-id="3c3cc-305">**YSize**</span><span class="sxs-lookup"><span data-stu-id="3c3cc-305">**YSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c3cc-306">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3c3cc-306">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3c3cc-307">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3c3cc-307">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3c3cc-308">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process and thread structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwYSize")</span><span class="sxs-lookup"><span data-stu-id="3c3cc-308">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|dwYSize")</span></span>
</dt> </dl>

<span data-ttu-id="3c3cc-309">Hauteur en pixels d’une fenêtre si une nouvelle fenêtre est créée.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-309">Pixel height of a window if a new window is created.</span></span> <span data-ttu-id="3c3cc-310">Pour les processus d’interface utilisateur graphique, cette méthode est utilisée uniquement la première fois que le nouveau processus appelle [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) pour créer une fenêtre avec chevauchement si le paramètre *nWidth* de **CreateWindow** est **CW \_ usedefault**.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-310">For GUI processes, this is used only the first time the new process calls [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) to create an overlapped window if the *nWidth* parameter of **CreateWindow** is **CW\_USEDEFAULT**.</span></span>

> [!Note]  
> <span data-ttu-id="3c3cc-311">**XSIZE** et **YSize** ne peuvent pas être spécifiés indépendamment.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-311">**XSize** and **YSize** cannot be specified independently.</span></span>

 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3c3cc-312">Notes</span><span class="sxs-lookup"><span data-stu-id="3c3cc-312">Remarks</span></span>

<span data-ttu-id="3c3cc-313">Cette classe est dérivée de [**Win32 \_ MethodParameterClass**](win32-methodparameterclass.md).</span><span class="sxs-lookup"><span data-stu-id="3c3cc-313">This class is derived from [**Win32\_MethodParameterClass**](win32-methodparameterclass.md).</span></span>

<span data-ttu-id="3c3cc-314">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="3c3cc-314">Overview</span></span>

<span data-ttu-id="3c3cc-315">La méthode de [**création**](create-method-in-class-win32-process.md) de [**\_ processus Win32**](win32-process.md) vous permet de configurer les options de démarrage pour tout nouveau processus s’exécutant sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-315">The [**Win32\_Process**](win32-process.md) [**Create**](create-method-in-class-win32-process.md) method enables you to configure startup options for any new process running on a computer.</span></span> <span data-ttu-id="3c3cc-316">Par exemple, vous pouvez configurer un processus de manière à ce qu’il démarre dans une fenêtre « masquée », ce qui empêche un utilisateur de voir et éventuellement de l’interrompre.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-316">For example, you can configure a process so that it starts in a "hidden" window, which prevents a user from seeing, and possibly interrupting, it.</span></span> <span data-ttu-id="3c3cc-317">Si le processus s’exécute dans une fenêtre de commande, vous pouvez configurer la taille, le titre, les couleurs de premier plan et d’arrière-plan de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-317">If the process runs in a command window, you can configure the size, title, and foreground and background colors of the window.</span></span>

<span data-ttu-id="3c3cc-318">Les options de démarrage sont configurées à l’aide de la classe **Win32 \_ ProcessStartup** .</span><span class="sxs-lookup"><span data-stu-id="3c3cc-318">Startup options are configured using the **Win32\_ProcessStartup** class.</span></span> <span data-ttu-id="3c3cc-319">**Win32 \_ ProcessStartup** est une classe de type méthode ; la classe de type de méthode existe uniquement pour passer des informations à une méthode.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-319">**Win32\_ProcessStartup** is a Method Type class; the Method Type class exists solely to pass information to a method.</span></span> <span data-ttu-id="3c3cc-320">Dans ce cas, toutes les propriétés d’une instance de **\_ ProcessStartup Win32** sont passées à une instance du [**\_ processus Win32**](win32-process.md).</span><span class="sxs-lookup"><span data-stu-id="3c3cc-320">In this case, all the properties of an instance of **Win32\_ProcessStartup** are passed to an instance of [**Win32\_Process**](win32-process.md).</span></span>

<span data-ttu-id="3c3cc-321">**Utilisation de Win32 \_ ProcessStartup**</span><span class="sxs-lookup"><span data-stu-id="3c3cc-321">**Using Win32\_ProcessStartup**</span></span>

1.  <span data-ttu-id="3c3cc-322">Créez une instance de **\_ ProcessStartup Win32**.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-322">Create an instance of **Win32\_ProcessStartup**.</span></span>
2.  <span data-ttu-id="3c3cc-323">Configurez les propriétés de la nouvelle instance.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-323">Configure the properties of the new instance.</span></span>
3.  <span data-ttu-id="3c3cc-324">Incluez l’instance dans le cadre de la méthode de création de [**\_ processus Win32**](win32-process.md) .</span><span class="sxs-lookup"><span data-stu-id="3c3cc-324">Include the instance as part of the [**Win32\_Process**](win32-process.md) Create method.</span></span>

<span data-ttu-id="3c3cc-325">Par exemple, si vous avez créé une **instance \_ ProcessStartup Win32** nommée objConfig, vous devez passer le nom de l’objet dans la méthode Create comme suit :</span><span class="sxs-lookup"><span data-stu-id="3c3cc-325">For example, if you have created a **Win32\_ProcessStartup** instance named objConfig, you would pass the object name in the Create method as follows:</span></span>

`errReturn = objProcess.Create("Database.exe", null, objConfig, intProcessID)`

## <a name="examples"></a><span data-ttu-id="3c3cc-326">Exemples</span><span class="sxs-lookup"><span data-stu-id="3c3cc-326">Examples</span></span>

<span data-ttu-id="3c3cc-327">Vous pouvez utiliser la classe **Win32 \_ ProcessStartup** pour configurer différentes options de démarrage pour un processus.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-327">You can use the **Win32\_ProcessStartup** class to configure various startup options for a process.</span></span> <span data-ttu-id="3c3cc-328">Ces options incluent, sans s’y limiter, des choses telles que la création d’un processus dans une fenêtre masquée et la création d’un processus de priorité plus élevée.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-328">These options include, but are not limited to, such things as creating a process in a hidden window and creating a higher-priority process.</span></span> <span data-ttu-id="3c3cc-329">Le code VBScript suivant crée un processus dans une fenêtre masquée.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-329">The following VBScript creates a process in a hidden window.</span></span>


```VB
Const HIDDEN_WINDOW = 12
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objStartup = objWMIService.Get("Win32_ProcessStartup")
Set objConfig = objStartup.SpawnInstance_
objConfig.ShowWindow = HIDDEN_WINDOW
Set objProcess = GetObject("winmgmts:root\cimv2:Win32_Process")
errReturn = objProcess.Create("Notepad.exe", null, objConfig, intProcessID)
```



<span data-ttu-id="3c3cc-330">Le code VBScript suivant crée un processus de priorité plus élevée.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-330">The following VBScript creates a higher-priority process.</span></span>


```VB
Const ABOVE_NORMAL = 32768
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objStartup = objWMIService.Get("Win32_ProcessStartup")
Set objConfig = objStartup.SpawnInstance_
objConfig.PriorityClass = ABOVE_NORMAL
Set objProcess = GetObject("winmgmts:root\cimv2:Win32_Process")
objProcess.Create "Database.exe", Null, objConfig, intProcessID
```



<span data-ttu-id="3c3cc-331">L’exemple de code VBScript suivant crée un processus Notepad sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-331">The following VBScript code example creates a Notepad process on the local computer.</span></span> <span data-ttu-id="3c3cc-332">**Win32 \_ ProcessStartup** est utilisé pour configurer les paramètres de processus.</span><span class="sxs-lookup"><span data-stu-id="3c3cc-332">**Win32\_ProcessStartup** is used to configure the process settings.</span></span>


```VB
Const SW_NORMAL = 1
strComputer = "."
strCommand = "Notepad.exe" 
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

' Configure the Notepad process to show a window
Set objStartup = objWMIService.Get("Win32_ProcessStartup")
Set objConfig = objStartup.SpawnInstance_
objConfig.ShowWindow = SW_NORMAL

' Create Notepad process
Set objProcess = objWMIService.Get("Win32_Process")
intReturn = objProcess.Create _
    (strCommand, Null, objConfig, intProcessID)
If intReturn <> 0 Then
    Wscript.Echo "Process could not be created." & vbNewLine & _
                 "Command line: " & strCommand & vbNewLine & _
                 "Return value: " & intReturn
Else
    Wscript.Echo "Process created." & vbNewLine & _
                 "Command line: " & strCommand & vbNewLine & _
                 "Process ID: " & intProcessID
End If
```



## <a name="requirements"></a><span data-ttu-id="3c3cc-333">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3c3cc-333">Requirements</span></span>



| <span data-ttu-id="3c3cc-334">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3c3cc-334">Requirement</span></span> | <span data-ttu-id="3c3cc-335">Valeur</span><span class="sxs-lookup"><span data-stu-id="3c3cc-335">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c3cc-336">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c3cc-336">Minimum supported client</span></span><br/> | <span data-ttu-id="3c3cc-337">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3c3cc-337">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3c3cc-338">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c3cc-338">Minimum supported server</span></span><br/> | <span data-ttu-id="3c3cc-339">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3c3cc-339">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3c3cc-340">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3c3cc-340">Namespace</span></span><br/>                | <span data-ttu-id="3c3cc-341">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="3c3cc-341">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3c3cc-342">MOF</span><span class="sxs-lookup"><span data-stu-id="3c3cc-342">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3c3cc-343"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3c3cc-343"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3c3cc-344">DLL</span><span class="sxs-lookup"><span data-stu-id="3c3cc-344">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c3cc-345"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c3cc-345"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c3cc-346">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c3cc-346">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c3cc-347">**\_MethodParameterClass Win32**</span><span class="sxs-lookup"><span data-stu-id="3c3cc-347">**Win32\_MethodParameterClass**</span></span>](win32-methodparameterclass.md)
</dt> <dt>

[<span data-ttu-id="3c3cc-348">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="3c3cc-348">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="3c3cc-349">**\_Processus Win32**</span><span class="sxs-lookup"><span data-stu-id="3c3cc-349">**Win32\_Process**</span></span>](win32-process.md)
</dt> <dt>

[<span data-ttu-id="3c3cc-350">**\_\_ProviderHostQuotaConfiguration**</span><span class="sxs-lookup"><span data-stu-id="3c3cc-350">**\_\_ProviderHostQuotaConfiguration**</span></span>](../wmisdk/--providerhostquotaconfiguration.md)
</dt> <dt>

[<span data-ttu-id="3c3cc-351">Tâches WMI : processus</span><span class="sxs-lookup"><span data-stu-id="3c3cc-351">WMI Tasks: Processes</span></span>](../wmisdk/wmi-tasks--processes.md)
</dt> </dl>

 

 
