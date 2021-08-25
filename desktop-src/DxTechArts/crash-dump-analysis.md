---
title: 'Analyse de vidage sur plantage '
description: Cet article technique fournit des informations sur l’écriture et l’utilisation d’un minidump.
ms.assetid: 575c4716-18c2-7b11-7308-aa2e3d8efac7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3c68891e2e20938036bd016e6e786a2cdad0096ae44af0e8974a88052963be0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075519"
---
# <a name="crash-dump-analysis"></a>Analyse de vidage sur plantage 

Tous les bogues ne peuvent pas être détectés avant la mise en version, ce qui signifie que tous les bogues qui lèvent des exceptions peuvent être détectés avant la publication. Heureusement, Microsoft a inclus dans le kit de développement logiciel (SDK) de plate-forme une fonction pour aider les développeurs à collecter des informations sur les exceptions découvertes par les utilisateurs. La fonction [**entrée**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) écrit les informations de vidage sur incident nécessaires dans un fichier sans enregistrer la totalité de l’espace de traitement. Ce fichier d’informations de vidage sur incident est appelé minidump. Cet article technique fournit des informations sur l’écriture et l’utilisation d’un minidump.

-   [Écriture d’un minidump](#writing-a-minidump)
-   [Sécurité des threads](#thread-safety)
-   [Écriture d’un minidump avec du code](#writing-a-minidump-with-code)
-   [Utilisation de Dumpchk.exe](#using-dumpchkexe)
-   [Analyse d’un minidump](#analyzing-a-minidump)
    -   [Utilisation du serveur de symboles publics Microsoft](#using-the-microsoft-public-symbol-server)
    -   [Débogage d’un minidump avec WinDbg](#debugging-a-minidump-with-windbg)
    -   [Utilisation d’outils de Copy-Protection avec minidumps](#using-copy-protection-tools-with-minidumps)
-   [Résumé](#summary)

## <a name="writing-a-minidump"></a>Écriture d’un minidump

Les options de base pour l’écriture d’un minidump sont les suivantes :

-   Ne rien faire. Windows génère automatiquement un minidump chaque fois qu’un programme lève une exception non gérée. la génération automatique d’un minidump est disponible depuis Windows XP. si l’utilisateur l’autorise, le minidump sera envoyé à Microsoft, et non pas au développeur, via Rapport d’erreurs Windows (WER). les développeurs peuvent accéder à ces minidumps via le [programme d’Application de bureau Windows](../appxpkg/windows-desktop-application-program.md).

    L’utilisation de WER requiert les éléments suivants :

    -   Développeurs pour signer leurs applications à l’aide d’Authenticode
    -   Les applications ont une ressource VERSIONINFO valide dans chaque fichier exécutable et DLL

    Si vous implémentez une routine personnalisée pour les exceptions non gérées, vous êtes fortement invité à utiliser la fonction [**ReportFault**](/windows/desktop/api/errorrep/nf-errorrep-reportfault) dans le gestionnaire d’exceptions pour envoyer également un minidump automatisé à wer. La fonction **ReportFault** gère tous les problèmes de connexion et d’envoi du Minidump à wer. Ne pas envoyer de minidumps à WER ne respecte pas les exigences des jeux pour Windows.

    pour plus d’informations sur le fonctionnement de WER, consultez fonctionnement de [Rapport d’erreurs Windows](https://www.microsoft.com/whdc/maintain/WER/WERWorks.mspx). pour obtenir une explication des détails de l’inscription, consultez [présentation de Rapport d’erreurs Windows](https://msdn.microsoft.com/) dans la [Zone ISV](https://msdn.microsoft.com/)de MSDN.

-   utilisez un produit de la Microsoft Visual Studio Team System. Dans le menu **Déboguer** , cliquez sur **enregistrer le dump sous** pour enregistrer une copie d’un vidage. L’utilisation d’un vidage enregistré localement n’est qu’une option de test et de débogage interne.
-   Ajoutez du code à votre projet. Ajoutez la fonction [**entrée**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) et le code de gestion des exceptions approprié pour enregistrer et envoyer un minidump directement au développeur. Cet article montre comment implémenter cette option. toutefois, notez que **entrée** ne fonctionne pas actuellement avec du code managé et n’est disponible que sur Windows XP, Windows Vista, Windows 7.

## <a name="thread-safety"></a>Sécurité des threads

[**Entrée**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) fait partie de la bibliothèque dbghelp. Cette bibliothèque n’est pas thread-safe, donc tout programme qui utilise **entrée** doit synchroniser tous les threads avant de tenter d’appeler **entrée**.

## <a name="writing-a-minidump-with-code"></a>Écriture d’un minidump avec du code

L’implémentation réelle est simple. Voici un exemple simple d’utilisation de [**entrée**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump).


```C++
#include <dbghelp.h>
#include <shellapi.h>
#include <shlobj.h>

int GenerateDump(EXCEPTION_POINTERS* pExceptionPointers)
{
    BOOL bMiniDumpSuccessful;
    WCHAR szPath[MAX_PATH]; 
    WCHAR szFileName[MAX_PATH]; 
    WCHAR* szAppName = L"AppName";
    WCHAR* szVersion = L"v1.0";
    DWORD dwBufferSize = MAX_PATH;
    HANDLE hDumpFile;
    SYSTEMTIME stLocalTime;
    MINIDUMP_EXCEPTION_INFORMATION ExpParam;

    GetLocalTime( &stLocalTime );
    GetTempPath( dwBufferSize, szPath );

    StringCchPrintf( szFileName, MAX_PATH, L"%s%s", szPath, szAppName );
    CreateDirectory( szFileName, NULL );

    StringCchPrintf( szFileName, MAX_PATH, L"%s%s\\%s-%04d%02d%02d-%02d%02d%02d-%ld-%ld.dmp", 
               szPath, szAppName, szVersion, 
               stLocalTime.wYear, stLocalTime.wMonth, stLocalTime.wDay, 
               stLocalTime.wHour, stLocalTime.wMinute, stLocalTime.wSecond, 
               GetCurrentProcessId(), GetCurrentThreadId());
    hDumpFile = CreateFile(szFileName, GENERIC_READ|GENERIC_WRITE, 
                FILE_SHARE_WRITE|FILE_SHARE_READ, 0, CREATE_ALWAYS, 0, 0);

    ExpParam.ThreadId = GetCurrentThreadId();
    ExpParam.ExceptionPointers = pExceptionPointers;
    ExpParam.ClientPointers = TRUE;

    bMiniDumpSuccessful = MiniDumpWriteDump(GetCurrentProcess(), GetCurrentProcessId(), 
                    hDumpFile, MiniDumpWithDataSegs, &ExpParam, NULL, NULL);

    return EXCEPTION_EXECUTE_HANDLER;
}


void SomeFunction()
{
    __try
    {
        int *pBadPtr = NULL;
        *pBadPtr = 0;
    }
    __except(GenerateDump(GetExceptionInformation()))
    {
    }
}
```



Cet exemple illustre l’utilisation de base de [**entrée**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) et les informations minimales nécessaires pour l’appeler. Le nom du fichier de vidage est celui du développeur. Toutefois, pour éviter les collisions de noms de fichiers, il est recommandé de générer le nom de fichier à partir du nom et du numéro de version de l’application, des ID de processus et de thread, ainsi que de la date et de l’heure. Cela permet également de conserver les minidumps regroupés par application et par version. Il revient au développeur de déterminer la quantité d’informations qui est utilisée pour différencier les noms de fichiers minidump.

Notez que le nom du chemin d’accès dans l’exemple précédent a été généré en appelant la fonction [**GetTempPath**](/windows/desktop/api/fileapi/nf-fileapi-gettemppatha) pour récupérer le chemin d’accès du répertoire désigné pour les fichiers temporaires. L’utilisation de ce répertoire fonctionne même avec les comptes d’utilisateur dotés de privilèges minimum, et il empêche également le Minidump d’occuper de l’espace disque après qu’il n’est plus nécessaire.

Si vous archivez le produit pendant votre processus de génération quotidien, veillez également à inclure des symboles pour la build afin de pouvoir déboguer une ancienne version du produit, si nécessaire. Vous devez également prendre des mesures pour gérer les optimisations complètes du compilateur tout en générant des symboles. Pour ce faire, ouvrez les propriétés de votre projet dans l’environnement de développement et, pour la configuration Release, procédez comme suit :

1.  Sur le côté gauche de la page de propriétés du projet, cliquez sur C/C++. Par défaut, cette option affiche les paramètres **généraux** . Sur le côté droit de la page de propriétés du projet, définissez **format des informations de débogage** sur **base de données du programme (/ZI)**.
2.  Sur le côté gauche de la page de propriétés, développez **éditeur de liens**, puis cliquez sur **débogage**. Sur le côté droit de la page de propriétés, affectez à **générer des informations de débogage** la valeur **Oui (/Debug)**.
3.  Cliquez sur **optimisation**, puis définissez les **références** à E liminate les **données non référencées (/OPT : REF)**.
4.  Définissez **activer le repli COMDAT** pour **Supprimer les COMDAT redondants (/OPT : ICF)**.

MSDN contient des informations plus détaillées sur la structure d’informations sur les [**\_ exceptions \_ de Minidump**](/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_exception_information) et la fonction [**entrée**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) .

## <a name="using-dumpchkexe"></a>Utilisation de Dumpchk.exe

Dumpchk.exe est un utilitaire de ligne de commande qui peut être utilisé pour vérifier qu’un fichier de vidage a été créé correctement. Si Dumpchk.exe génère une erreur, cela signifie que le fichier de vidage est endommagé et ne peut pas être analysé. Pour plus d’informations sur l’utilisation de Dumpchk.exe, consultez [comment utiliser Dumpchk.exe pour vérifier un fichier d’image mémoire](https://support.microsoft.com/kb/315271/).

Dumpchk.exe est inclus sur le cd-rom du produit Windows XP et peut être installé sur les \\ outils de prise en charge des fichiers programme du lecteur système \\ \\ en exécutant Setup.exe dans le \\ dossier outils de support du \\ CD Windows XP. vous pouvez également vous procurer la dernière version de Dumpchk.exe en téléchargeant et en installant les outils de débogage disponibles à partir de [Windows outils de débogage](https://www.microsoft.com/whdc/devtools/debugging/) sur [Windows matériel developer Central](https://www.microsoft.com/whdc/).

## <a name="analyzing-a-minidump"></a>Analyse d’un minidump

L’ouverture d’un minidump pour l’analyse est aussi simple que d’en créer un.

**Pour analyser un minidump**

1.  Ouvrez Visual Studio.
2.  Dans le menu **fichier** , cliquez sur **ouvrir Project**.
3.  Définissez **fichiers de type** sur **fichiers dump**, accédez au fichier dump, sélectionnez-le, puis cliquez sur **Ouvrir.**
4.  Exécutez le débogueur.

Le débogueur crée un processus simulé. Le processus simulé sera arrêté au niveau de l’instruction qui a provoqué l’incident.

### <a name="using-the-microsoft-public-symbol-server"></a>Utilisation du serveur de symboles publics Microsoft

pour obtenir la pile pour les pannes au niveau du pilote ou du système, il peut être nécessaire de configurer Visual Studio pour qu’il pointe vers le serveur de symboles publics Microsoft.

**Pour définir un chemin d’accès au serveur de symboles Microsoft**

1.  Dans le menu **Déboguer** , cliquez sur **options**.
2.  Dans la boîte de dialogue **options** , ouvrez le nœud **débogage** , puis cliquez sur **symboles**.
3.  Assurez **-vous que la recherche dans les emplacements ci-dessus uniquement lorsque les symboles sont chargés manuellement** n’est pas sélectionnée, à moins que vous ne souhaitiez charger manuellement les symboles lors du débogage.
4.  Si vous utilisez des symboles sur un serveur de symboles distant, vous pouvez améliorer les performances en spécifiant un répertoire local dans lequel les symboles peuvent être copiés. Pour ce faire, entrez un chemin d’accès pour les **symboles de cache du serveur de symboles vers ce répertoire**. Pour vous connecter au serveur de symboles publics Microsoft, vous devez activer ce paramètre. Notez que si vous déboguez un programme sur un ordinateur distant, le répertoire de cache fait référence à un répertoire sur l’ordinateur distant.
5.  Cliquez sur **OK**.
6.  Étant donné que vous utilisez le serveur de symboles publics Microsoft, une boîte de dialogue contrat de licence utilisateur final s’affiche. Cliquez sur **Oui** pour accepter le contrat et télécharger des symboles dans votre cache local.

### <a name="debugging-a-minidump-with-windbg"></a>Débogage d’un minidump avec WinDbg

vous pouvez également utiliser WinDbg, un débogueur qui fait partie des outils de débogage Windows, pour déboguer un minidump. WinDbg vous permet de déboguer sans avoir à utiliser Visual Studio. pour télécharger Windows outils de débogage, consultez [Windows outils de débogage](https://www.microsoft.com/whdc/devtools/debugging/) sur [Windows matériel developer Central](https://www.microsoft.com/whdc/).

après avoir installé Windows outils de débogage, vous devez entrer le chemin d’accès aux symboles dans WinDbg.

**Pour entrer un chemin d’accès aux symboles dans WinDbg**

1.  Dans le menu **fichier** , cliquez sur **chemin d’accès aux symboles**.
2.  Dans la fenêtre **chemin de recherche de symboles** , entrez les informations suivantes :

    « SRV \* c : \\ cache \* https://msdl.microsoft.com/download/symbols ; »

### <a name="using-copy-protection-tools-with-minidumps"></a>Utilisation d’outils de Copy-Protection avec minidumps

Les développeurs doivent également savoir comment leur schéma de protection contre la copie peut affecter le minidump. La plupart des schémas de protection contre la copie ont leurs propres outils de déchiffrement, et il appartient au développeur d’apprendre à utiliser ces outils avec [**entrée**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump).

## <a name="summary"></a>Résumé

La fonction [**entrée**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) peut être un outil extrêmement utile pour la collecte et la résolution des bogues une fois que le produit a été publié. L’écriture d’un gestionnaire d’exceptions personnalisé qui utilise **entrée** permet au développeur de personnaliser la collection d’informations et d’améliorer le processus de débogage. La fonction est suffisamment flexible pour être utilisée dans n’importe quel projet basé sur C++ et doit être considérée comme faisant partie du processus de stabilité du projet.

 

 