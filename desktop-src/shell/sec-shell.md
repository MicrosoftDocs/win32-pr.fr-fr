---
description: Cette rubrique fournit des informations sur les considérations relatives à la sécurité de l’interpréteur de commandes Windows.
ms.assetid: eca31652-2659-456d-b082-c84d6fd39094
title: 'Considérations relatives à la sécurité : Microsoft Windows Shell'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16b11a965a36a403b57a3e5229fc758a4ce37252
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753045"
---
# <a name="security-considerations-microsoft-windows-shell"></a>Considérations relatives à la sécurité : Microsoft Windows Shell

Cette rubrique fournit des informations sur les considérations relatives à la sécurité de l’interpréteur de commandes Windows. Ce document ne peut pas vous fournir tout ce que vous devez savoir sur les problèmes de sécurité. Utilisez-le plutôt comme point de départ et référence pour ce domaine technologique spécifique.

L’interpréteur de commandes contrôle plusieurs aspects importants du système, y compris ceux qui présentent des risques de sécurité potentiels s’ils ne sont pas correctement gérés. Cette rubrique décrit certains des problèmes les plus courants et comment les résoudre dans vos applications. N’oubliez pas que la sécurité n’est pas limitée aux attaques basées sur Internet. Sur les systèmes partagés, y compris les systèmes accessibles par le biais des services Terminal Server, vous devez également vous assurer que les utilisateurs ne peuvent pas faire quoi que ce soit pour nuire à ceux qui partagent le système.

-   [Installation correcte de votre application](#installing-your-application-properly)
-   [Shlwapi](#shlwapi)
-   [Saisie semi-automatique](#autocomplete)
-   [ShellExecute, ShellExecuteEx et fonctions connexes](#shellexecute-shellexecuteex-and-related-functions)
-   [Déplacement et copie de fichiers](#moving-and-copying-files)
-   [Écriture d’extensions d’espace de noms sécurisées](#writing-secure-namespace-extensions)
-   [alertes de sécurité](#security-alerts)
-   [Rubriques connexes](#related-topics)

## <a name="installing-your-application-properly"></a>Installation correcte de votre application

La majorité des problèmes potentiels de sécurité de l’interpréteur de commandes peuvent être atténués en installant correctement votre application.

-   Installez l’application dans le dossier Program Files. 

    | Système d’exploitation                             | Emplacement                                                                                                                                                                                                                                   |
    |----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Windows XP, Windows Server 2003 et versions antérieures | \_fichiers programme \_ CSIDL                                                                                                                                                                                                                      |
    | Windows Vista et versions ultérieures                      | FOLDERID \_ ProgramFiles, FOLDERID \_ PROGRAMFILESX86, FOLDERID \_ ProgramFilesX64, FOLDERID \_ ProgramFilesCommon, FOLDERID \_ ProgramFilesCommonX86 ou FOLDERID ProgramFilesCommonX64 \_ . Consultez [**KNOWNFOLDERID**](knownfolderid.md) pour plus de détails. |

    

     

-   Ne stockez pas les données utilisateur dans le dossier Program Files.

    Utilisez le dossier de données approprié pour les données qui sont communes à tous les utilisateurs.

    

    | Système d’exploitation                             | Emplacement               |
    |----------------------------------------------|------------------------|
    | Windows XP, Windows Server 2003 et versions antérieures | CSIDL \_ Common \_ AppData |
    | Windows Vista et versions ultérieures                      | FOLDERID \_ ProgramData  |

    

     

    Utilisez le dossier des données utilisateur approprié pour les données qui appartiennent à un utilisateur particulier.

    

    | Système d’exploitation                             | Emplacement                                                   |
    |----------------------------------------------|------------------------------------------------------------|
    | Windows XP, Windows Server 2003 et versions antérieures | CSIDL \_ AppData, CSIDL \_ Personal et d’autres.               |
    | Windows Vista et versions ultérieures                      | FOLDERID \_ RoamingAppData, FOLDERID \_ documents et autres. |

    

     

-   Si vous devez installer dans un autre emplacement que le dossier Program Files, veillez à définir correctement les listes de contrôle d’accès (ACL) afin que les utilisateurs n’aient pas accès aux parties inappropriées du système de fichiers. Toutes les données spécifiques à un utilisateur particulier doivent avoir une liste de contrôle d’accès qui empêche tout autre utilisateur d’y accéder.
-   Quand vous configurez des associations de fichiers, veillez à spécifier correctement la ligne de commande. Utilisez un chemin d’accès qualifié complet et encapsulez tous les éléments qui contiennent des espaces blancs entre guillemets. Encapsulez les paramètres de commande entre guillemets distincts. Dans le cas contraire, la chaîne peut être analysée de manière incorrecte et l’application ne démarrera pas correctement. Deux exemples de lignes de commande correctement formées sont affichés ici.

    ```
    "C:\Program Files\MyApp\MyApp.exe" "%1" "%2"
    C:\MyAppDir\MyApp\MyApp.exe "%1"
    ```

    

> [!Note]  
> L’emplacement des dossiers d’installation standard peut varier d’un système à un système. Pour obtenir l’emplacement d’un dossier standard sur un système Windows Vista ou ultérieur donné, appelez [**SHGetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) avec la valeur [**KNOWNFOLDERID**](knownfolderid.md) appropriée. Dans Windows XP, Windows Server 2003 ou les systèmes antérieurs, appelez [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) ou [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) avec la valeur [**CSIDL**](csidl.md) appropriée.

 

## <a name="shlwapi"></a>Shlwapi

L’API légère de Shell (shlwapi) comprend un certain nombre de fonctions de manipulation de chaînes. L’utilisation incorrecte de ces fonctions peut entraîner des chaînes tronquées de manière inattendue sans notification de la troncation retournée. Dans les cas suivants, les fonctions shlwapi ne doivent pas être utilisées. Les autres fonctions listées, qui présentent moins de risques, doivent être utilisées à leur place.



| Shlwapi, fonction                                                 | Autre fonction                                                                                             |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**Strcat**](/windows/desktop/api/Shlwapi/nf-shlwapi-strcatw),[**StrNCat**](/windows/desktop/api/Shlwapi/nf-shlwapi-strncata)              | [**StringCchCat**](/windows/win32/api/strsafe/nf-strsafe-stringcchcata), [**StringCbCat**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata) et fonctions connexes             |
| [**Strcpy**](/windows/desktop/api/Shlwapi/nf-shlwapi-strcpyw), [ **StrCpyN**](/windows/desktop/api/Shlwapi/nf-shlwapi-strcpynw)             | [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya), [**StringCbCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopya) et fonctions connexes         |
| [**wnsprintf**](/windows/desktop/api/Shlwapi/nf-shlwapi-wnsprintfa), [ **wvnsprintf**](/windows/desktop/api/Shlwapi/nf-shlwapi-wvnsprintfa) | [**StringCchPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcchprintfa), [**StringCbPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfa) et fonctions connexes |



 

Avec des fonctions telles que [**PathRelativePathTo**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathrelativepathtoa) qui retournent un chemin d’accès de fichier, définissez toujours la taille de la mémoire tampon sur des \_ caractères de chemin d’accès maximaux. Cela permet de s’assurer que la mémoire tampon est suffisamment grande pour contenir le plus grand chemin de fichier possible, plus un caractère null de fin.

Pour plus d’informations sur les autres fonctions de chaîne, consultez [à propos de strsafe. h](../menurc/strsafe-ovw.md).

## <a name="autocomplete"></a>Autocomplétion

N’utilisez pas la fonctionnalité de saisie semi-automatique pour les mots de passe.

## <a name="shellexecute-shellexecuteex-and-related-functions"></a>ShellExecute, ShellExecuteEx et fonctions connexes

Vous pouvez utiliser plusieurs fonctions de l’interpréteur de commandes pour lancer des applications : [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec)et [**SHCreateProcessAsUserW**](/windows/desktop/api/Shellapi/nf-shellapi-shcreateprocessasuserw). Veillez à fournir une définition non ambiguë de l’application qui doit être exécutée.

-   Lorsque vous fournissez le chemin d’accès du fichier exécutable, indiquez le chemin d’accès complet. Ne dépendez pas de l’interpréteur de commandes pour localiser le fichier.
-   Si vous fournissez une chaîne de ligne de commande qui contient des espaces blancs, encapsulez la chaîne entre guillemets. Dans le cas contraire, l’analyseur peut interpréter un élément unique qui contient des espaces comme plusieurs éléments.

## <a name="moving-and-copying-files"></a>Déplacement et copie de fichiers

L’une des clés de la sécurité du système est l’attribution correcte des listes de contrôle d’accès. Vous pouvez également utiliser des fichiers chiffrés. Lorsque vous déplacez ou copiez des fichiers, assurez-vous qu’ils reçoivent la liste de contrôle d’accès correcte et qu’ils n’ont pas été déchiffrés par inadvertance. Cela comprend le déplacement de fichiers vers la **Corbeille**, ainsi que dans le système de fichiers. Utilisez [**IFileOperation**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation) (Windows Vista ou version ultérieure) ou [**SHFILEOPERATION**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) (Windows XP et versions antérieures). N’utilisez pas [**MoveFile**](/windows/win32/api/winbase/nf-winbase-movefile), qui peut ne pas définir la liste de contrôle d’accès attendue pour le fichier de destination.

## <a name="writing-secure-namespace-extensions"></a>Écriture d’extensions d’espace de noms sécurisées

Les extensions d’espace de noms de Shell sont un moyen puissant et flexible de présenter des données à l’utilisateur. Toutefois, ils peuvent provoquer une défaillance du système s’ils ne sont pas correctement écrits. Voici quelques points clés à garder à l’esprit :

-   Ne partez pas du principe que les données telles que les images sont mises en forme correctement.
-   Ne supposez pas que \_ le chemin d’accès maximal est équivalent au nombre d' *octets* dans une chaîne. Il s’agit du nombre de *caractères*.

## <a name="security-alerts"></a>Alertes de sécurité

Le tableau suivant répertorie certaines fonctionnalités qui peuvent, si elles sont utilisées de manière incorrecte, compromettre la sécurité de vos applications.



| Fonctionnalité                                                                        | Limitation des risques                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), [ **ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) | Les recherches qui dépendent de la vérification d’une série d’emplacements par défaut pour rechercher un fichier spécifique peuvent être utilisées dans une attaque par usurpation d’identité. Utilisez un chemin d’accès complet pour vous assurer d’accéder au fichier souhaité.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**StrCat**](/windows/desktop/api/Shlwapi/nf-shlwapi-strcatw)                                                       | Le premier argument, *psz1*, doit être suffisamment grand pour contenir *psz2* et le' \\ 0 'fermant, sinon, un dépassement de mémoire tampon peut se produire. Utilisez plutôt l’une des alternatives suivantes. [**StringCbCat**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata), [**StringCbCatEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatexa), [**StringCbCatN**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatna), [**StringCbCatNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatnexa), [**StringCchCat**](/windows/win32/api/strsafe/nf-strsafe-stringcchcata), [**StringCchCatEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatexa), [**StringCchCatN**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatna)ou [**StringCchCatNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatnexa).                                                                                                                                                             |
| [**StrCatBuff**](/windows/desktop/api/Shlwapi/nf-shlwapi-strcatbuffa)                                               | Il n’est pas garanti que la dernière chaîne se termine par un caractère null. Utilisez plutôt l’une des alternatives suivantes. [**StringCbCat**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata), [**StringCbCatEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatexa), [**StringCbCatN**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatna), [**StringCbCatNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatnexa), [**StringCchCat**](/windows/win32/api/strsafe/nf-strsafe-stringcchcata), [**StringCchCatEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatexa), [**StringCchCatN**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatna)ou [**StringCchCatNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatnexa).                                                                                                                                                                                                                                  |
| [**StrCatChainW**](/windows/desktop/api/Shlwapi/nf-shlwapi-strcatchainw)                                           | Il n’est pas garanti que la dernière chaîne se termine par un caractère null. Utilisez plutôt l’une des alternatives suivantes. [**StringCbCatEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatexa), [**StringCbCatNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatnexa), [**StringCchCatEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatexa)ou [**StringCchCatNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatnexa).                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**StrCpy**](/windows/desktop/api/Shlwapi/nf-shlwapi-strcpyw)                                                       | Le premier argument, *psz1*, doit être suffisamment grand pour contenir *psz2* et le' \\ 0 'fermant, sinon, un dépassement de mémoire tampon peut se produire. Utilisez plutôt l’une des alternatives suivantes. [**StringCbCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopya), [**StringCbCopyEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopyexa), [**StringCbCopyN**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopyna), [**StringCbCopyNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopynexa), [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya), [**StringCchCopyEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopyexa), [**StringCchCopyN**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopyna)ou [**StringCchCopyNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopynexa).                                                                                                                                             |
| [**StrCpyN**](/windows/desktop/api/Shlwapi/nf-shlwapi-strcpynw)                                                     | Il n’est pas garanti que la chaîne copiée se termine par un caractère null. Utilisez plutôt l’une des alternatives suivantes. [**StringCbCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopya), [**StringCbCopyEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopyexa), [**StringCbCopyN**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopyna), [**StringCbCopyNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopynexa), [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya), [**StringCchCopyEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopyexa), [**StringCchCopyN**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopyna), [**StringCchCopyNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopynexa).                                                                                                                                                                                                                    |
| [**StrDup**](/windows/desktop/api/Shlwapi/nf-shlwapi-strdupa)                                                       | [**StrDup**](/windows/desktop/api/Shlwapi/nf-shlwapi-strdupa) suppose que *lpsz* est une chaîne terminée par le caractère null. En outre, il n’est pas garanti que la chaîne retournée soit terminée par un caractère null. Utilisez plutôt l’une des alternatives suivantes. [**StringCbCat**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata), [**StringCbCopyEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopyexa), [**StringCbCopyN**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopyna), [**StringCbCopyNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopynexa), [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya), [**StringCchCopyEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopyexa), [**StringCchCopyN**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopyna)ou [**StringCchCopyNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopynexa).                                                                                                                              |
| [**StrNCat**](/windows/desktop/api/Shlwapi/nf-shlwapi-strncata)                                                     | Le premier argument, *pszFront*, doit être suffisamment grand pour contenir *pszBack* et le' \\ 0 'fermant, sinon, un dépassement de mémoire tampon peut se produire. N’oubliez pas que le dernier argument, *cchMax*, est le nombre de caractères à copier dans *pszFront*, pas nécessairement la taille du *pszFront* en octets. Utilisez plutôt l’une des alternatives suivantes. [**StringCbCat**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata), [**StringCbCatEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatexa), [**StringCbCatN**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatna), [**StringCbCatNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatnexa), [**StringCchCat**](/windows/win32/api/strsafe/nf-strsafe-stringcchcata), [**StringCchCatEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatexa), [**StringCchCatN**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatna)ou [**StringCchCatNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatnexa). |
| [**wnsprintf**](/windows/desktop/api/Shlwapi/nf-shlwapi-wnsprintfa)                                                 | Il n’est pas garanti que la chaîne copiée se termine par un caractère null. Utilisez plutôt l’une des alternatives suivantes. [**StringCbPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfa), [**StringCbPrintfEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfexa), [**StringCbVPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbvprintfa), [**StringCbVPrintfEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbvprintfexa), [**StringCchPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcchprintfa), [**StringCchPrintfEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchprintfexa), [**StringCchVPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcchvprintfa)ou [**StringCchVPrintfEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchvprintfexa).                                                                                                                                                                                 |
| [**wvnsprintf**](/windows/desktop/api/Shlwapi/nf-shlwapi-wvnsprintfa)                                               | Il n’est pas garanti que la chaîne copiée se termine par un caractère null. Utilisez plutôt l’une des alternatives suivantes. [**StringCbPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfa), [**StringCbPrintfEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfexa), [**StringCbVPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbvprintfa), [**StringCbVPrintfEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbvprintfexa), [**StringCchPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcchprintfa), [**StringCchPrintfEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchprintfexa), [**StringCchVPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcchvprintfa)ou [**StringCchVPrintfEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchvprintfexa).                                                                                                                                                                                 |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Sécurité Microsoft](https://www.microsoft.com/security/default.aspx)
</dt> <dt>

[Centre de développement Sécurité](https://msdn.microsoft.com/security/)
</dt> <dt>

[Microsoft Solution Accelerators](/previous-versions/tn-archive/cc936627(v=technet.10))
</dt> <dt>

[Centre de Sécurité TechNet](https://technet.microsoft.com/security/default.aspx)
</dt> <dt>

[À propos de strsafe. h](../menurc/strsafe-ovw.md)
</dt> </dl>

 

 
