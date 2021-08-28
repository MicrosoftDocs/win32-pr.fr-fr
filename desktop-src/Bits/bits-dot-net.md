---
title: Utilisation de BITS à partir de .NET à l’aide de dll de référence
description: Les exemples suivants montrent comment appeler l’interface COM BITS à partir d’un programme .NET
ms.assetid: 1058970C-CE81-47D6-950E-3B6289E956B6
ms.topic: article
ms.date: 11/13/2018
ms.openlocfilehash: 00f7d6287d86dd1816d7e4b0a7c6e18c9ae4916c5c85b01d0280758cf9d00b5b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529149"
---
# <a name="calling-into-bits-from-net-and-c-using-reference-dlls"></a>Appel de BITS à partir de .NET et C# à l’aide de dll de référence

l’une des façons d’appeler les classes COM bits à partir d’un programme .net consiste à créer un fichier DLL de référence à partir des fichiers [IDL](/windows/desktop/Midl/midl-start-page) bits (Interface Definition Language) dans le SDK Windows, à l’aide des outils [MIDL](/windows/desktop/Midl/using-the-midl-compiler-2) et [TLBIMP](/dotnet/framework/tools/tlbimp-exe-type-library-importer) . La DLL de référence est un ensemble de wrappers de classe pour les classes COM BITS ; vous pouvez ensuite utiliser les classes wrapper directement à partir de .NET.

une alternative à l’utilisation de dll de référence créées automatiquement consiste à utiliser un wrapper .net BITS tiers à partir de [GitHub](https://github.com/) et [NuGet](https://www.nuget.org/). Ces wrappers ont souvent un style de programmation .NET plus naturel, mais ils peuvent dépasser les modifications et les mises à jour dans les interfaces BITS.

## <a name="creating-the-reference-dlls"></a>Création des dll de référence
### <a name="bits-idl-files"></a>Fichiers IDL BITS

Vous allez commencer par le jeu de fichiers IDL BITS. Il s’agit de fichiers qui définissent entièrement l’interface COM BITS. les fichiers se trouvent dans le répertoire **Windows Kits** et sont nommés bits *version*. idl (par exemple, bits10_2. idl), à l’exception du fichier version 1,0 qui est simplement bits. idl. À mesure que de nouvelles versions de BITS sont créées, de nouveaux fichiers IDL BITS sont également créés.

Vous pouvez également modifier une copie des fichiers IDL du kit de développement logiciel (SDK) BITS pour utiliser les fonctionnalités BITS qui ne sont pas automatiquement converties en équivalents .NET. Les modifications possibles des fichiers IDL sont décrites plus loin sur.

Les fichiers IDL BITS incluent plusieurs autres fichiers IDL par référence. Elles s’imbriquent également, de sorte que si vous utilisez une version, elle comprend toutes les versions inférieures.

Pour chaque version de BITS que vous souhaitez cibler dans votre programme, vous avez besoin d’une DLL de référence pour cette version. Par exemple, si vous souhaitez écrire un programme qui fonctionne sur BITS 1,5 et versions, mais qui a des fonctionnalités supplémentaires lorsque BITS 10,2 est présent, vous devez convertir les fichiers bits1_5. idl et bits10_2. idl.


### <a name="midl-and-tlbimp-utilities"></a>Utilitaires MIDL et TLBIMP

L’utilitaire [MIDL](/windows/desktop/Midl/using-the-midl-compiler-2) (Microsoft Interface Definition Language) convertit les fichiers IDL qui décrivent l’interface com bits en un fichier TLB (bibliothèque de types). L’outil MIDL dépend de l’utilitaire CL (préprocesseur C) pour lire correctement le fichier de langage IDL. l’utilitaire CL fait partie de Visual Studio et est installé lorsque vous incluez des fonctionnalités C/C++ dans l’installation Visual Studio.

L’utilitaire MIDL crée normalement un ensemble de fichiers C et H (code de langage C et en-tête de langage C). Vous pouvez supprimer ces fichiers supplémentaires en envoyant la sortie à l’appareil NUL :. Par exemple, si vous définissez le commutateur/dlldata NUL :, vous supprimez la création d’un fichier dlldata. c. Les exemples de commandes ci-dessous montrent les commutateurs qui doivent être définis sur NUL :.

L’utilitaire [Tlbimp](/dotnet/framework/tools/tlbimp-exe-type-library-importer) (importateur de bibliothèques de types) lit un fichier TLB et crée le fichier dll de référence correspondant. 


### <a name="example-commands-for-midl-and-tlbimp"></a>Exemples de commandes pour MIDL et TLBIMP

Voici un exemple de l’ensemble complet de commandes permettant de générer un ensemble de fichiers de référence. vous devrez peut-être modifier les commandes en fonction de votre Visual Studio et SDK Windows installation et en fonction des fonctionnalités BITS et des versions de système d’exploitation que vous ciblez. 

L’exemple crée un répertoire pour placer les fichiers DLL de référence et crée une variable d’environnement BITSTEMP pour pointer vers ce répertoire. 

les exemples de commandes exécutent ensuite le fichier vsdevcmd.bat créé par le programme d’installation de Visual Studio. Ce fichier BAT configure vos chemins d’accès et certaines variables d’environnement afin que les commandes MIDL et TLBIMP s’exécutent. il configure également les variables WindowsSdkDir et WindowsSDKLibVersion pour qu’elles pointent vers les répertoires SDK Windows les plus récents.

```console
REM Create a working directory
REM You can select a different directory based on your needs.
SET BITSTEMP=C:\BITSTEMPDIR
MKDIR "%BITSTEMP%"

REM Run the VsDevCmd.bat file to locate the Windows
REM SDK directory and the tools directories
REM This will be different for different versions of
REM Visual Studio

CALL "C:\Program Files (x86)\Microsoft Visual Studio\2017\Enterprise\Common7\Tools\vsdevcmd.bat"

REM Run the MIDL command on the desired BITS IDL file
REM This will generate a TLB file for the TLBIMP command
REM The IDL file will be different depending on which
REM set of BITS interfaces you need to use.
REM Run the MIDL command once per reference file
REM that you will need to explicitly use.
PUSHD .
CD /D "%WindowsSdkDir%Include\%WindowsSDKLibVersion%um"

MIDL  /I ..\shared /out "%BITSTEMP%" bits1_5.idl /dlldata NUL: /header NUL: /iid NUL: /proxy NUL:
MIDL  /I ..\shared /out "%BITSTEMP%" bits4_0.idl /dlldata NUL: /header NUL: /iid NUL: /proxy NUL:
MIDL  /I ..\shared /out "%BITSTEMP%" bits5_0.idl /dlldata NUL: /header NUL: /iid NUL: /proxy NUL:
MIDL  /I ..\shared /out "%BITSTEMP%" bits10_1.idl /dlldata NUL: /header NUL: /iid NUL: /proxy NUL:
MIDL  /I ..\shared /out "%BITSTEMP%" bits10_2.idl /dlldata NUL: /header NUL: /iid NUL: /proxy NUL:

REM Run the TLBIMP command on the resulting TLB file(s)
REM Try to keep a parallel set of names.
TLBIMP "%BITSTEMP%"\bits1_5.tlb /out: "%BITSTEMP%"\BITSReference1_5.dll
TLBIMP "%BITSTEMP%"\bits4_0.tlb /out: "%BITSTEMP%"\BITSReference4_0.dll
TLBIMP "%BITSTEMP%"\bits5_0.tlb /out: "%BITSTEMP%"\BITSReference5_0.dll
TLBIMP "%BITSTEMP%"\bits10_1.tlb /out: "%BITSTEMP%"\BITSReference10_1.dll
TLBIMP "%BITSTEMP%"\bits10_2.tlb /out: "%BITSTEMP%"\BITSReference10_2.dll
DEL "%BITSTEMP%"\bits*.tlb
POPD

```
Une fois ces commandes exécutées, vous disposez d’un ensemble de dll de référence dans le répertoire BITSTEMP.

### <a name="adding-the-reference-dlls-to-your-project"></a>Ajout des dll de référence à votre projet

Pour utiliser une DLL de référence dans un projet C#, ouvrez votre projet C# dans Visual Studio. Dans le Explorateur de solutions, cliquez avec le bouton droit sur les références, puis cliquez sur Ajouter une référence. Cliquez ensuite sur le bouton Parcourir, puis sur le bouton Ajouter. Accédez au répertoire contenant les dll de référence, sélectionnez-les, puis cliquez sur Ajouter. Dans la fenêtre Gestionnaire de références, les dll de référence sont vérifiées. Puis cliquez sur OK.

Les dll de référence BITS sont maintenant ajoutées à votre projet.

Les informations contenues dans les fichiers DLL de référence sont incorporées dans votre programme final. Vous n’avez pas besoin d’expédier les fichiers DLL de référence avec votre programme ; vous devez simplement expédier le .EXE. 

Vous pouvez modifier si les dll de référence sont incorporées dans le fichier EXE final. Utilisez la propriété [incorporer les types Interop](/dotnet/framework/interop/how-to-add-references-to-type-libraries) pour déterminer si les dll de référence seront incorporées. Cette opération peut être effectuée en fonction de la référence. La valeur par défaut est true pour incorporer les dll.

## <a name="modifying-idl-files-for-more-complete-net-code"></a>Modification des fichiers IDL pour obtenir du code .NET plus complet

Les fichiers IDL BITS (Microsoft Interface Definition Language) peuvent être utilisés sans modification pour créer le fichier DLL BackgroundCopyManager. Toutefois, il manque des unions non convertibles à la DLL de référence .NET obtenue et des noms difficiles à utiliser s’affichent pour certaines structures et certains enums. Cette section décrit quelques-unes des modifications que vous pouvez apporter pour rendre la DLL .NET plus complète et plus facile à utiliser.

### <a name="simpler-enum-names"></a>Noms d’ENUM plus simples

Les fichiers IDL BITS définissent généralement des valeurs enum comme suit :
```
    typedef enum
    {
            BG_AUTH_TARGET_SERVER = 1,
            BG_AUTH_TARGET_PROXY
    } BG_AUTH_TARGET;
```
Le BG_AUTH_TARGET est le nom du typedef ; l’enum réel n’est pas nommé. Cela ne provoque généralement pas de problèmes avec le code C, mais ne se traduit pas correctement pour une utilisation avec un programme .NET. Un nouveau nom est créé automatiquement, mais il peut ressembler à _MIDL___MIDL_itf_bits4_0_0005_0001_0001 au lieu d’une valeur explicite. Vous pouvez résoudre ce problème en mettant à jour les fichiers MIDL pour inclure un nom d’enum.

```
    typedef enum BG_AUTH_TARGET
    {
            BG_AUTH_TARGET_SERVER = 1,
            BG_AUTH_TARGET_PROXY
    } BG_AUTH_TARGET;
```

Le nom enum peut être le même que le nom typedef. Certains programmeurs ont une convention d’affectation de noms dans laquelle ils sont conservés différents (par exemple, en plaçant un trait de soulignement avant le nom de l’enum), mais cela ne perturbe que les traductions .NET. 

### <a name="string-types-in-unions"></a>Types chaîne dans les unions

Les fichiers IDL BITS passent des chaînes à l’aide de la Convention LPWSTR (long pointer vers une chaîne de caractères larges). Bien que cela fonctionne lors du passage de paramètres de fonction (tels que la méthode Job. GetDisplayName ([out] LPWSTR * pVal)), cela ne fonctionne pas lorsque les chaînes font partie d’unions. Par exemple, le fichier bits5_0. idl comprend le BITS_FILE_PROPERTY_VALUE Union :

```
typedef [switch_type(BITS_FILE_PROPERTY_ID)] union
{
    [case( BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS )]
        LPWSTR String;
}
BITS_FILE_PROPERTY_VALUE;
```

Le champ LPWSTR n’est pas inclus dans la version .NET de l’Union. Pour résoudre ce problème, remplacez le LPWSTR par un WCHAR *. Le champ résultant (appelé chaîne) est passé en tant que IntPtr. Convertissez-le en une chaîne à l’aide de System. Runtime. InteropServices. Marshal. PtrToStringAuto (valeur. Chaîne); méthode.

### <a name="unions-in-structures"></a>Unions dans les structures

Parfois, les unions incorporées dans des structures ne sont pas incluses dans la structure. Par exemple, dans le Bits1_5. idl, la BG_AUTH_CREDENTIALS est définie comme suit :
```
    typedef struct
    {
        BG_AUTH_TARGET Target;
        BG_AUTH_SCHEME Scheme;
        [switch_is(Scheme)] BG_AUTH_CREDENTIALS_UNION Credentials;
    }
    BG_AUTH_CREDENTIALS;
```

La BG_AUTH_CREDENTIALS_UNION est définie comme étant une Union comme suit :
```
    typedef [switch_type(BG_AUTH_SCHEME)] union
    {
            [case( BG_AUTH_SCHEME_BASIC, BG_AUTH_SCHEME_DIGEST, BG_AUTH_SCHEME_NTLM,
            BG_AUTH_SCHEME_NEGOTIATE, BG_AUTH_SCHEME_PASSPORT )] BG_BASIC_CREDENTIALS Basic;
            [default] ;
    } BG_AUTH_CREDENTIALS_UNION;
```
Le champ des informations d’identification dans le BG_AUTH_CREDENTIALS ne sera pas inclus dans la définition de la classe .NET.

Notez que l’Union est définie pour toujours être une BG_BASIC_CREDENTIALS indépendamment des BG_AUTH_SCHEME. Étant donné que l’Union n’est pas utilisée en tant qu’Union, nous pouvons simplement transmettre un BG_BASIC_CREDENTIALS comme suit :
```
    typedef struct
    {
        BG_AUTH_TARGET Target;
        BG_AUTH_SCHEME Scheme;
        BG_BASIC_CREDENTIALS Credentials;
    }
    BG_AUTH_CREDENTIALS;
```

## <a name="using-bits-from-c"></a>Utilisation de BITS à partir de C #

### <a name="recommended-using-statement"></a>Instruction using recommandée

La configuration d’instructions using en C# réduira le nombre de caractères que vous devez taper pour utiliser les différentes versions BITS. Le nom « BITSReference » provient du nom de la DLL de référence.

```csharp
// Set up the BITS namespaces
using BITS = BITSReference1_5;
using BITS4 = BITSReference4_0;
using BITS5 = BITSReference5_0;
using BITS10_2 = BITSReference10_2;
```

### <a name="quick-sample-download-a-file"></a>Exemple rapide : télécharger un fichier

Un extrait de code C# pour télécharger un fichier à partir d’une URL est fourni ci-dessous. 

```csharp
    var mgr = new BITS.BackgroundCopyManager1_5();
    BITS.GUID jobGuid;
    BITS.IBackgroundCopyJob job;
    mgr.CreateJob("Quick download", BITS.BG_JOB_TYPE.BG_JOB_TYPE_DOWNLOAD, out jobGuid, out job);
    job.AddFile("https://aka.ms/WinServ16/StndPDF", @"C:\Server2016.pdf");
    job.Resume();
    bool jobIsFinal = false;
    while (!jobIsFinal)
    {
        BITS.BG_JOB_STATE state;
        job.GetState(out state);
        switch (state)
        {
            case BITS.BG_JOB_STATE.BG_JOB_STATE_ERROR:
            case BITS.BG_JOB_STATE.BG_JOB_STATE_TRANSFERRED:
                job.Complete();
                break;

            case BITS.BG_JOB_STATE.BG_JOB_STATE_CANCELLED:
            case BITS.BG_JOB_STATE.BG_JOB_STATE_ACKNOWLEDGED:
                jobIsFinal = true;
                break;
            default:
                Task.Delay(500); // delay a little bit
                break;
        }
    }
    // Job is complete
```

Dans cet exemple de code, un gestionnaire de BITS nommé Mgr est créé. Il correspond directement à l’interface [IBackgroundCopyManager](/windows/desktop/api/bits/nn-bits-ibackgroundcopymanager) . 

À partir du gestionnaire, un nouveau travail est créé. Le travail est un paramètre de sortie sur la méthode CreateJob. Le nom du travail (qui n’a pas besoin d’être unique) et le type de téléchargement, qui est un travail de téléchargement, sont également transmis. Un GUID BITS pour l’identificateur de tâche est également renseigné.

Une fois la tâche créée, vous ajoutez un nouveau fichier de téléchargement au travail avec la méthode AddFile. Vous devez passer deux chaînes, une pour le fichier distant (l’URL ou le partage de fichiers) et l’autre pour le fichier local. 

Après avoir ajouté le fichier, appelez Resume sur le travail pour le démarrer. Ensuite, le code attend jusqu’à ce que le travail soit dans un état final (erreur ou transféré), puis soit terminé.

### <a name="bits-versions-casting-and-queryinterface"></a>Versions BITS, Cast et QueryInterface

Vous constaterez que vous devez souvent utiliser une version antérieure d’un objet BITS et une version plus récente dans votre programme.  

Par exemple, lorsque vous créez un objet de traitement, vous obtiendrez un méthode ibackgroundcopyjob (partie de la version de BITS 1,0) même si vous le faites à l’aide d’un objet gestionnaire plus récent et qu’un objet méthode ibackgroundcopyjob plus récent est disponible. Étant donné que la méthode CreateJob n’accepte pas d’interface pour la version la plus récente, vous ne pouvez pas créer directement la version la plus récente.

Utilisez un cast .NET pour convertir un objet de type antérieur en un objet de type plus récent. Le cast appellera automatiquement une QueryInterface COM si nécessaire. 

Dans cet exemple, il existe un objet méthode ibackgroundcopyjob BITS nommé « job » et nous voulons le convertir en un objet IBackgroundCopyJob5 nommé « JOB5 » afin de pouvoir appeler la méthode BITS 5,0 GetProperty. Nous venons d’effectuer un cast vers le type IBackgroundCopyJob5 comme suit :

```csharp
var job5 = (BITS5.IBackgroundCopyJob5)job;
```

La variable JOB5 sera initialisée par .NET à l’aide de la fonction QueryInterface correcte. 

Si votre code peut s’exécuter sur un système qui ne prend pas en charge une version particulière de BITS, vous pouvez essayer le cast et intercepter System. InvalidCastException. 

```csharp
BITS5.IBackgroundCopyJob5 job5 = null;
try
{
    job5 = (BITS5.IBackgroundCopyJob5)Job;
}
catch (System.InvalidCastException)
{
    ; // Must be running an earlier version of BITS
}
```

Un problème courant se pose lorsque vous essayez d’effectuer un cast en un type d’objet incorrect. Le système .NET ne connaît pas la relation réelle entre les interfaces BITS. Si vous demandez un genre d’interface incorrect, .NET tentera de le faire pour vous et échouera avec une exception InvalidCastException et HResult 0x80004002 (E_NOINTERFACE).

### <a name="working-with-bits-versions-10_1-and-10_2"></a>Utilisation des versions BITS 10_1 et 10_2

sur certaines versions de Windows 10 vous ne pouvez pas créer directement un objet IBackgroundCopyManager BITS à l’aide des interfaces 10,1 ou 10,2. Au lieu de cela, vous devrez utiliser plusieurs versions des fichiers de référence de la DLL BackgroundCopyManager. Par exemple, vous pouvez utiliser la version 1,5 pour créer un objet IBackgroundCopyManager, puis effectuer un cast des objets de tâche ou de fichier résultants à l’aide des versions 10,1 ou 10,2.

