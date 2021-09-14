---
description: la \_ classe WMI ProcessStartup abstraite Win32 représente la configuration de démarrage d’un processus basé sur Windows.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127124249"
---
# <a name="win32_processstartup-class"></a>\_Classe ProcessStartup Win32

la [classe WMI](../wmisdk/retrieving-a-class.md) **\_ ProcessStartup** abstraite Win32 représente la configuration de démarrage d’un processus basé sur Windows. La classe est définie comme une définition de type de méthode, ce qui signifie qu’elle est utilisée uniquement pour passer des informations à la méthode [**Create**](create-method-in-class-win32-process.md) de la classe de [**\_ processus Win32**](win32-process.md) .

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

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

## <a name="members"></a>Membres

La classe **Win32 \_ ProcessStartup** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ ProcessStartup** a ces propriétés.

<dl> <dt>

**CreateFlags**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Process and thread Functions \| [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) \| dwCreationFlags »)
</dt> </dl>

Valeurs supplémentaires qui contrôlent la classe de priorité et la création du processus. Les valeurs de création suivantes peuvent être spécifiées dans n’importe quelle combinaison, sauf indication contraire.

<dt>

<span id="Debug_Process"></span><span id="debug_process"></span><span id="DEBUG_PROCESS"></span>

<span id="Debug_Process"></span><span id="debug_process"></span><span id="DEBUG_PROCESS"></span>**Débogage \_ Processus** (1)


</dt> <dd>

Si cet indicateur est défini, le processus appelant est traité comme un débogueur et le nouveau processus est en cours de débogage. Le système notifie le débogueur de tous les événements de débogage qui se produisent dans le processus en cours de débogage.

</dd> <dt>

<span id="Debug_Only_This_Process"></span><span id="debug_only_this_process"></span><span id="DEBUG_ONLY_THIS_PROCESS"></span>

<span id="Debug_Only_This_Process"></span><span id="debug_only_this_process"></span><span id="DEBUG_ONLY_THIS_PROCESS"></span>**Débogage \_ Uniquement \_ ce \_ processus** (2)


</dt> <dd>

Si cet indicateur n’est pas défini et que le processus appelant est en cours de débogage, le nouveau processus devient un autre processus en cours de débogage. Si le processus appelant n’est pas un processus de débogage, aucune action relative au débogage ne se produit.

</dd> <dt>

<span id="Create_Suspended"></span><span id="create_suspended"></span><span id="CREATE_SUSPENDED"></span>

<span id="Create_Suspended"></span><span id="create_suspended"></span><span id="CREATE_SUSPENDED"></span>**Créer \_ Suspendu** (4)


</dt> <dd>

Le thread principal du nouveau processus est créé dans un état suspendu et ne s’exécute pas tant que la méthode [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) n’est pas appelée.

</dd> <dt>

<span id="Detached_Process"></span><span id="detached_process"></span><span id="DETACHED_PROCESS"></span>

<span id="Detached_Process"></span><span id="detached_process"></span><span id="DETACHED_PROCESS"></span>**Détaché \_ Processus** (8)


</dt> <dd>

Pour les processus de console, le nouveau processus n’a pas accès à la console du processus parent. Cet indicateur ne peut pas être utilisé si l’indicateur **créer \_ un nouvel ensemble de \_ console** est défini.

</dd> <dt>

<span id="Create_New_Console"></span><span id="create_new_console"></span><span id="CREATE_NEW_CONSOLE"></span>

<span id="Create_New_Console"></span><span id="create_new_console"></span><span id="CREATE_NEW_CONSOLE"></span>**Créer \_ Nouvelle \_ console** (16)


</dt> <dd>

Ce nouveau processus a une nouvelle console, au lieu d’hériter de la console parente. Cet indicateur ne peut pas être utilisé avec l’indicateur de **\_ processus détaché** .

</dd> <dt>

<span id="Create_New_Process_Group"></span><span id="create_new_process_group"></span><span id="CREATE_NEW_PROCESS_GROUP"></span>

<span id="Create_New_Process_Group"></span><span id="create_new_process_group"></span><span id="CREATE_NEW_PROCESS_GROUP"></span>**Créer \_ Nouveau \_ \_ groupe de processus** (512)


</dt> <dd>

Ce nouveau processus est le processus racine d’un nouveau groupe de processus. Le groupe de processus comprend tous les processus qui sont des descendants de ce processus racine. L’identificateur de processus du nouveau groupe de processus est le même que celui qui est retourné dans la propriété **ProcessID** de la classe de [**\_ processus Win32**](win32-process.md) . Les groupes de processus sont utilisés par la méthode [**GenerateConsoleCtrlEvent**](/windows/console/generateconsolectrlevent) pour permettre l’envoi d’un signal Ctrl + C ou d’un signal CTRL + ATTN à un groupe de processus de console.

</dd> <dt>

<span id="Create_Unicode_Environment"></span><span id="create_unicode_environment"></span><span id="CREATE_UNICODE_ENVIRONMENT"></span>

<span id="Create_Unicode_Environment"></span><span id="create_unicode_environment"></span><span id="CREATE_UNICODE_ENVIRONMENT"></span>**Créer \_ \_Environnement Unicode** (1024)


</dt> <dd>

Les paramètres d’environnement listés dans la propriété **EnvironmentVariables** utilisent des caractères Unicode. Si cet indicateur n’est pas défini, le bloc d’environnement utilise des caractères ANSI.

</dd> <dt>

<span id="Create_Default_Error_Mode"></span><span id="create_default_error_mode"></span><span id="CREATE_DEFAULT_ERROR_MODE"></span>

<span id="Create_Default_Error_Mode"></span><span id="create_default_error_mode"></span><span id="CREATE_DEFAULT_ERROR_MODE"></span>**Créer \_ \_ \_ Mode d’erreur par défaut** (67108864)


</dt> <dd>

Les processus qui viennent d’être créés reçoivent le mode d’erreur système par défaut du processus appelant au lieu d’hériter du mode d’erreur du processus parent. Cet indicateur est utile pour les applications Shell multithread qui s’exécutent avec des erreurs matérielles désactivées.

</dd> <dt>

<span id="CREATE_BREAKAWAY_FROM_JOB"></span><span id="create_breakaway_from_job"></span>

<span id="CREATE_BREAKAWAY_FROM_JOB"></span><span id="create_breakaway_from_job"></span>**Créer \_ DISSOCIation \_ d’un \_ travail** (16777216)


</dt> <dd>

Utilisé pour le processus créé qui ne doit pas être limité par l’objet de traitement.

</dd> </dl>

</dd> <dt>

**EnvironmentVariables**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| HKEY \_ Current \_ User \\ \\ Environment")
</dt> </dl>

Liste de paramètres pour la configuration d’un ordinateur. Les variables d’environnement spécifient des chemins de recherche pour les fichiers, les répertoires de fichiers temporaires, les options spécifiques à l’application et d’autres informations similaires. Le système gère un bloc de paramètres d’environnement pour chaque utilisateur et un pour l’ordinateur. Le bloc environnement système représente les variables d’environnement pour tous les utilisateurs d’un ordinateur spécifique. Le bloc environnement d’un utilisateur représente les variables d’environnement gérées par le système pour un utilisateur spécifique, et comprend l’ensemble des variables d’environnement système. Par défaut, chaque processus reçoit une copie du bloc d’environnement pour son processus parent. En règle générale, il s’agit du bloc d’environnement de l’utilisateur qui a ouvert une session. Un processus peut spécifier différents blocs d’environnement pour ses processus enfants.

</dd> <dt>

**ErrorMode**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Error Functions \| SetErrorMode »)
</dt> </dl>

Sur certains processeurs non x86, les références de mémoire mal alignées provoquent une exception d’erreur d’alignement. L’option **aucune \_ faute d’alignement, \_ \_ à l’exception** de l’indicateur, vous permet de contrôler si un système d’exploitation corrige automatiquement ces erreurs d’alignement ou s’il les rend visibles pour une application. Sur une plateforme de millions d’instructions par seconde (MIPS), une application doit appeler explicitement [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) avec la faute d’alignement, à l' **\_ \_ \_ exception** de flag pour que le système d’exploitation corrige automatiquement les erreurs d’alignement.

Comment un système d’exploitation traite plusieurs types d’erreurs graves. Vous pouvez spécifier que le système d’exploitation traite les erreurs ou qu’une application puisse recevoir et traiter les erreurs.

Le paramètre par défaut permet au système d’exploitation de rendre visibles les erreurs d’alignement pour une application. Étant donné que la plateforme x86 ne rend pas les erreurs d’alignement visibles pour une application, l’absence d’erreur d' **\_ alignement, à l' \_ \_ exception** de Flag, ne fait pas échouer le système d’exploitation, même si l’indicateur n’est pas défini. L’État par défaut de [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) consiste à affecter à tous les indicateurs la valeur 0 (zéro).

<dt>



 (1)


</dt> <dd>

Default

</dd> <dt>

<span id="Fail_Critical_Errors"></span><span id="fail_critical_errors"></span><span id="FAIL_CRITICAL_ERRORS"></span>

<span id="Fail_Critical_Errors"></span><span id="fail_critical_errors"></span><span id="FAIL_CRITICAL_ERRORS"></span>**Échec \_ \_Erreurs critiques** (2)


</dt> <dd>

Si cet indicateur est défini, le système d’exploitation n’affiche pas la boîte de message du gestionnaire d’erreurs critiques lorsqu’une telle erreur se produit. Au lieu de cela, le système d’exploitation envoie l’erreur au processus appelant.

</dd> <dt>

<span id="No_Alignment_Fault_Except"></span><span id="no_alignment_fault_except"></span><span id="NO_ALIGNMENT_FAULT_EXCEPT"></span>

<span id="No_Alignment_Fault_Except"></span><span id="no_alignment_fault_except"></span><span id="NO_ALIGNMENT_FAULT_EXCEPT"></span>**Non \_ Erreur d’alignement \_ \_ , sauf** (4)


</dt> <dd>

Si cet indicateur est défini, le système d’exploitation corrige automatiquement les erreurs d’alignement de la mémoire et les rend invisibles pour l’application. Cela est fait pour les processus d’appel et descendants. Cet indicateur s’applique uniquement aux processeurs RISC (Reduced Instruction Set Computing) et n’a aucun effet sur les processeurs x86.

</dd> <dt>

<span id="No_GP_Fault_Error_Box"></span><span id="no_gp_fault_error_box"></span><span id="NO_GP_FAULT_ERROR_BOX"></span>

<span id="No_GP_Fault_Error_Box"></span><span id="no_gp_fault_error_box"></span><span id="NO_GP_FAULT_ERROR_BOX"></span>**Non \_ \_Boîte de \_ message \_ d’erreur de stratégie de défaut** (8)


</dt> <dd>

Si cet indicateur est défini, le système d’exploitation n’affiche pas la boîte de message d’erreur de protection générale lorsqu’une erreur de stratégie de groupe se produit. Cet indicateur doit être défini uniquement par les applications de débogage qui gèrent les erreurs de stratégie de groupe.

</dd> <dt>

<span id="No_Open_File_Error_Box"></span><span id="no_open_file_error_box"></span><span id="NO_OPEN_FILE_ERROR_BOX"></span>

<span id="No_Open_File_Error_Box"></span><span id="no_open_file_error_box"></span><span id="NO_OPEN_FILE_ERROR_BOX"></span>**Non \_ \_Boîte de \_ message \_ d’erreur ouvrir le fichier** (16)


</dt> <dd>

Si cet indicateur est défini, le système d’exploitation n’affiche pas de boîte de message lorsqu’il ne parvient pas à trouver un fichier. Au lieu de cela, l’erreur est retournée au processus appelant. Cet indicateur est actuellement ignoré.

</dd> </dl>

</dd> <dt>

**FillAttribute**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process and thread structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwFillAttribute")
</dt> </dl>

Les couleurs de texte et d’arrière-plan si une nouvelle fenêtre de console est créée dans une application console. Ces valeurs sont ignorées dans les applications d’interface utilisateur graphique (GUI). Pour spécifier les couleurs de premier plan et d’arrière-plan, ajoutez les valeurs ensemble. Par exemple, pour avoir le type rouge (4) sur un arrière-plan bleu (16), définissez FillAttribute sur 20.

<dt>

1
</dt> <dd>

Bleu de premier plan \_

</dd> <dt>

2
</dt> <dd>

Vert de premier plan \_

</dd> <dt>

4
</dt> <dd>

Premier plan \_ rouge

</dd> <dt>

8
</dt> <dd>

Intensité du premier plan \_

</dd> <dt>

16
</dt> <dd>

Arrière-plan \_ bleu

</dd> <dt>

32
</dt> <dd>

Arrière-plan \_ vert

</dd> <dt>

64
</dt> <dd>

Arrière-plan \_ rouge

</dd> <dt>

128
</dt> <dd>

Intensité de l’arrière-plan \_

</dd> </dl>

</dd> <dt>

**PriorityClass**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Process and thread structures \| [**JOBOBJECT \_ Basic \_ Limit \_ information**](/windows/win32/api/winnt/ns-winnt-jobobject_basic_limit_information) \| PriorityClass »)
</dt> </dl>

Classe de priorité du nouveau processus. Utilisez cette propriété pour déterminer les priorités de planification des threads dans le processus. Si la propriété est laissée null, la classe Priority est définie par défaut sur normal, à moins que la classe de priorité du processus de création soit inactive ou inférieure à la \_ normale. Dans ce cas, le processus enfant reçoit la classe de priorité par défaut du processus appelant.

<dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (32)


</dt> <dd>

Indique un processus normal sans besoin de planification spécifique.

</dd> <dt>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Inactif** (64)


</dt> <dd>

Indique un processus avec des threads qui s’exécutent uniquement lorsque le système est inactif et qui sont précédés par les threads de tout processus s’exécutant dans une classe de priorité plus élevée. Par exemple, un écran de veille. La classe de priorité Idle est héritée par les processus enfants.

</dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>**Élevé** (128)


</dt> <dd>

Indique un processus qui exécute des tâches critiques à l’heure qui doivent être exécutées immédiatement pour s’exécuter correctement. Les threads d’un processus de classe de priorité élevée prévalent sur les threads de processus de classe de priorité normale ou d’inactivité. par exemple, Windows Liste des tâches, qui doit répondre rapidement lorsqu’il est appelé par l’utilisateur, quelle que soit la charge sur le système d’exploitation. Soyez extrêmement vigilant lorsque vous utilisez la classe de priorité élevée, car une application de classe haute priorité basée sur l’UC peut utiliser presque tous les cycles disponibles. Seule une priorité en temps réel anticipe les threads définis à ce niveau.

</dd> <dt>

<span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>

<span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>**Temps réel** (256)


</dt> <dd>

Indique un processus qui a la priorité la plus élevée possible. Les threads d’un processus de classe de priorité en temps réel devancent les threads de tous les autres processus, y compris les threads haute priorité et les processus du système d’exploitation qui effectuent des tâches importantes. Par exemple, un processus en temps réel qui s’exécute depuis plus d’un intervalle très court peut entraîner le vidage des caches de disque ou l’absence de réponse de la souris.

</dd> <dt>

<span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>

<span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>**Ci-dessous \_ Normal** (16384)


</dt> <dd>

Indique un processus dont la priorité est supérieure à inactif, mais inférieure à la normale.

</dd> <dt>

<span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>

<span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>**Ci-dessus \_ Normal** (32768)


</dt> <dd>

Indique un processus dont la priorité est supérieure à la normale mais inférieure à la valeur élevée.

</dd> </dl>

</dd> <dt>

**ShowWindow**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process and thread structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| wShowWindow")
</dt> </dl>

Mode d’affichage de la fenêtre pour l’utilisateur. Il peut s’agir de l’une des valeurs qui peuvent être spécifiées dans le paramètre *nCmdShow* pour la fonction [ShowWindow](/windows/desktop/api/winuser/nf-winuser-showwindow) .

</dd> <dt>

**Titre**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process and thread structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| lpTitle")
</dt> </dl>

Texte affiché dans la barre de titre lors de la création d’une nouvelle fenêtre de console ; utilisé pour les processus de console. Si la **valeur est null**, le nom du fichier exécutable est utilisé comme titre de la fenêtre. Cette propriété doit avoir la **valeur null** pour les processus d’interface utilisateur graphique ou de console qui ne créent pas de nouvelle fenêtre de console.

</dd> <dt>

**WinstationDesktop**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process and thread structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| lpDesktop")
</dt> </dl>

Le nom du bureau ou le nom du bureau et de la station Windows pour le processus. Une barre oblique inverse dans la chaîne indique que la chaîne comprend à la fois les noms de station de travail et de station Windows. Si **WinstationDesktop** a la **valeur null**, le nouveau processus hérite du bureau et de la station Windows de son processus parent. Si **WinstationDesktop** est une chaîne vide, le processus n’hérite pas du bureau et de la station Windows de son processus parent. Le système détermine si un nouveau bureau et une station Windows doivent être créés. Une station Windows est un objet sécurisé qui contient un presse-papiers, un ensemble d’atomes globaux et un groupe d’objets de bureau. La station de fenêtre interactive qui est assignée à la session d’ouverture de session de l’utilisateur interactif contient également le clavier, la souris et le périphérique d’affichage. Un bureau est un objet sécurisé contenu dans une station Windows. Un bureau a une surface d’affichage logique et contient des fenêtres, des menus et des crochets. Une station Windows peut avoir plusieurs bureaux. Seuls les ordinateurs de bureau de la station Windows Interactive peuvent être visibles et recevoir des entrées utilisateur.

</dd> <dt>

**X**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process and thread structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| DWX")
</dt> </dl>

Décalage X de l’angle supérieur gauche d’une fenêtre si une nouvelle fenêtre est créée, en pixels. Les décalages s’affichent dans le coin supérieur gauche de l’écran. Pour les processus d’interface utilisateur graphique, la position spécifiée est utilisée la première fois que le nouveau processus appelle [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) pour créer une fenêtre Overlapped si le paramètre *X* de **CreateWindow** est **CW \_ usedefault**.

> \[! Remarque X\]  
> et **Y** ne peuvent pas être spécifiés indépendamment.

 

</dd> <dt>

**XCountChars**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process and thread structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| XCountChars")
</dt> </dl>

Largeur de la mémoire tampon d’écran dans les colonnes de caractères. Cette propriété est utilisée pour les processus qui créent une fenêtre de console et est ignorée dans les processus GUI.

> [!Note]  
> **XCountChars** et **YCountChars** ne peuvent pas être spécifiés indépendamment.

 

</dd> <dt>

**XSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process and thread structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwXSize")
</dt> </dl>

Largeur en pixels d’une fenêtre si une nouvelle fenêtre est créée. Pour les processus GUI, cette méthode est utilisée uniquement la première fois que le nouveau processus appelle [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) pour créer une fenêtre avec chevauchement si le paramètre NWidth de **CreateWindow** est **CW \_ usedefault**.

> [!Note]  
> **XSIZE** et **YSize** ne peuvent pas être spécifiés indépendamment.

 

</dd> <dt>

**O**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process and thread structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwy")
</dt> </dl>

Décalage de pixel de l’angle supérieur gauche d’une fenêtre si une nouvelle fenêtre est créée. Les décalages proviennent de l’angle supérieur gauche de l’écran. Pour les processus d’interface utilisateur graphique, la position spécifiée est utilisée la première fois que le nouveau processus appelle [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) pour créer une fenêtre Overlapped si le paramètre *y* de **CreateWindow** est **CW \_ usedefault**.

> \[! Remarque X\]  
> et **Y** ne peuvent pas être spécifiés indépendamment.

 

</dd> <dt>

**YCountChars**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process and thread structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| YCountChars")
</dt> </dl>

Hauteur de la mémoire tampon d’écran dans les lignes de caractères. Cette propriété est utilisée pour les processus qui créent une fenêtre de console, mais elle est ignorée dans les processus GUI.

> [!Note]  
> **XCountChars** et **YCountChars** ne peuvent pas être spécifiés indépendamment.

 

</dd> <dt>

**YSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process and thread structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwYSize")
</dt> </dl>

Hauteur en pixels d’une fenêtre si une nouvelle fenêtre est créée. Pour les processus d’interface utilisateur graphique, cette méthode est utilisée uniquement la première fois que le nouveau processus appelle [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) pour créer une fenêtre avec chevauchement si le paramètre *nWidth* de **CreateWindow** est **CW \_ usedefault**.

> [!Note]  
> **XSIZE** et **YSize** ne peuvent pas être spécifiés indépendamment.

 

</dd> </dl>

## <a name="remarks"></a>Notes

Cette classe est dérivée de [**Win32 \_ MethodParameterClass**](win32-methodparameterclass.md).

Vue d’ensemble

La méthode de [**création**](create-method-in-class-win32-process.md) de [**\_ processus Win32**](win32-process.md) vous permet de configurer les options de démarrage pour tout nouveau processus s’exécutant sur un ordinateur. Par exemple, vous pouvez configurer un processus de manière à ce qu’il démarre dans une fenêtre « masquée », ce qui empêche un utilisateur de voir et éventuellement de l’interrompre. Si le processus s’exécute dans une fenêtre de commande, vous pouvez configurer la taille, le titre, les couleurs de premier plan et d’arrière-plan de la fenêtre.

Les options de démarrage sont configurées à l’aide de la classe **Win32 \_ ProcessStartup** . **Win32 \_ ProcessStartup** est une classe de type méthode ; la classe de type de méthode existe uniquement pour passer des informations à une méthode. Dans ce cas, toutes les propriétés d’une instance de **\_ ProcessStartup Win32** sont passées à une instance du [**\_ processus Win32**](win32-process.md).

**Utilisation de Win32 \_ ProcessStartup**

1.  Créez une instance de **\_ ProcessStartup Win32**.
2.  Configurez les propriétés de la nouvelle instance.
3.  Incluez l’instance dans le cadre de la méthode de création de [**\_ processus Win32**](win32-process.md) .

Par exemple, si vous avez créé une **instance \_ ProcessStartup Win32** nommée objConfig, vous devez passer le nom de l’objet dans la méthode Create comme suit :

`errReturn = objProcess.Create("Database.exe", null, objConfig, intProcessID)`

## <a name="examples"></a>Exemples

Vous pouvez utiliser la classe **Win32 \_ ProcessStartup** pour configurer différentes options de démarrage pour un processus. Ces options incluent, sans s’y limiter, des choses telles que la création d’un processus dans une fenêtre masquée et la création d’un processus de priorité plus élevée. Le code VBScript suivant crée un processus dans une fenêtre masquée.


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



Le code VBScript suivant crée un processus de priorité plus élevée.


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



l’exemple de code VBScript suivant crée un processus de Bloc-notes sur l’ordinateur local. **Win32 \_ ProcessStartup** est utilisé pour configurer les paramètres de processus.


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



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_MethodParameterClass Win32**](win32-methodparameterclass.md)
</dt> <dt>

[Classes du système d’exploitation](./operating-system-classes.md)
</dt> <dt>

[**\_Processus Win32**](win32-process.md)
</dt> <dt>

[**\_\_ProviderHostQuotaConfiguration**](../wmisdk/--providerhostquotaconfiguration.md)
</dt> <dt>

[Tâches WMI : processus](../wmisdk/wmi-tasks--processes.md)
</dt> </dl>

 

 
