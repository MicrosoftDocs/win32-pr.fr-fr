---
description: Limite de longueur maximale du chemin d’accès.
title: Limitation de longueur maximale du chemin
ms.topic: article
ms.custom: contperf-fy21q1
ms.date: 09/15/2020
ms.openlocfilehash: 4bf5050f24827a2033c1e56fd9413c04f4e59500
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127517813"
---
# <a name="maximum-path-length-limitation"></a>Limitation de longueur maximale du chemin

dans l’API Windows (avec quelques exceptions décrites dans les paragraphes suivants), la longueur maximale d’un chemin d’accès est le **\_ chemin d’accès** maximal, qui est défini sous la forme de 260 caractères. Un chemin d’accès local est structuré dans l’ordre suivant : lettre de lecteur, signe deux-points, barre oblique inverse, composants de nom séparés par des barres obliques inverses et caractère null de fin. Par exemple, le chemin d’accès maximal sur le lecteur D est « D : \\ *une chaîne de chemin d’accès de 256 caractères* &lt; &gt; nulle », où « &lt; nul &gt; » représente le caractère null de fin invisible pour la page de codes actuelle du système. (Les caractères < > sont utilisés ici pour une clarté visuelle et ne peuvent pas faire partie d’une chaîne de chemin d’accès valide.)

Par exemple, vous pouvez atteindre cette limitation si vous clonez un référentiel git qui contient des noms de fichiers longs dans un dossier qui a lui-même un nom long.


> [!Note]  
> les fonctions d’e/s de fichier de l’API Windows convertissent « / » en « » dans le cadre \\ de la conversion du nom en un nom de style NT, sauf en cas d’utilisation du \\ \\ \\ préfixe « ? », comme indiqué dans les sections suivantes.

l’API Windows possède de nombreuses fonctions qui ont également des versions Unicode pour autoriser un chemin d’accès de longueur étendue pour une longueur maximale du chemin d’accès de 32 767 caractères. Ce type de chemin d’accès est composé de composants séparés par des barres obliques inverses, jusqu’à la valeur retournée dans le paramètre *lpMaximumComponentLength* de la fonction [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) (cette valeur est généralement de 255 caractères). Pour spécifier un chemin d’accès de longueur étendue, utilisez le \\ \\ \\ préfixe «  ? ». Par exemple, « \\ \\ ? \\ D : \\ *chemin d’accès très long*».

> [!Note]  
> Le chemin d’accès maximal de 32 767 caractères est approximatif, car le \\ \\ \\ préfixe «  ? » peut être étendu à une chaîne plus longue par le système au moment de l’exécution, et cette expansion s’applique à la longueur totale.

Le \\ \\ \\ préfixe «  ? » peut également être utilisé avec les chemins d’accès construits selon la Convention d’affectation des noms (UNC). Pour spécifier un tel chemin d’accès à l’aide de l’UNC, utilisez le signe « \\ \\ ? \\ Préfixe UNC \\ . Par exemple, « \\ \\ ? \\ \\ \\ Partage de serveur UNC», où « serveur » est le nom de l’ordinateur et « partage » est le nom du dossier partagé. Ces préfixes ne sont pas utilisés dans le chemin d’accès lui-même. Elles indiquent que le chemin d’accès doit être passé au système avec une modification minimale, ce qui signifie que vous ne pouvez pas utiliser des barres obliques pour représenter des séparateurs de chemin d’accès, ou un point pour représenter le répertoire actif, ou des points doubles pour représenter le répertoire parent. Étant donné que vous ne pouvez pas utiliser le \\ \\ \\ préfixe «  ? » avec un chemin d’accès relatif, les chemins d’accès relatifs sont toujours limités à un nombre maximal de caractères de **chemin d' \_ accès** .

il n’est pas nécessaire d’effectuer une normalisation Unicode sur les chaînes de chemin d’accès et de nom de fichier pour une utilisation par les fonctions d’API d’e/s de fichier Windows, car le système de fichiers traite les noms de chemin et de fichier comme une séquence opaque de **WCHAR** s. toute normalisation nécessaire à votre application doit être effectuée avec cela à l’esprit, à l’extérieur des appels aux fonctions d’API d’e/s de fichier Windows associées.

Lors de l’utilisation d’une API pour créer un répertoire, le chemin d’accès spécifié ne peut pas être tellement long que vous ne pouvez pas ajouter un nom de fichier 8,3 (autrement dit, le nom du répertoire ne peut pas dépasser le **\_ chemin d’accès maximal** moins 12).

L’interpréteur de commandes et le système de fichiers ont des exigences différentes. il est possible de créer un chemin d’accès avec l’API Windows que l’interface utilisateur de l’interpréteur de commandes ne peut pas interpréter correctement.

## <a name="enable-long-paths-in-windows-10-version-1607-and-later"></a>activer les chemins d’accès longs dans Windows 10, Version 1607 et versions ultérieures

à partir de Windows 10, la version 1607, les limitations de **\_ chemin d’accès maximales** ont été supprimées des fonctions de répertoire et de fichier Win32 courantes. Toutefois, vous devez vous abonner au nouveau comportement.

Pour activer le nouveau comportement de chemin d’accès long, les deux conditions suivantes doivent être remplies :

* La clé de Registre `Computer\HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\FileSystem\LongPathsEnabled (Type: REG_DWORD)` doit exister et avoir la valeur 1. La valeur de la clé est mise en cache par le système (par processus) après le premier appel à une fonction de répertoire ou de fichier Win32 affectée (voir ci-dessous pour obtenir la liste des fonctions). La clé de registre ne sera pas rechargée pendant la durée de vie du processus. Pour que toutes les applications sur le système reconnaissent la valeur de la clé, un redémarrage peut être nécessaire car certains processus peuvent avoir démarré avant que la clé ait été définie.

Vous pouvez également copier ce code dans un `.reg` fichier qui peut le définir pour vous, ou utiliser la commande PowerShell à partir d’une fenêtre de terminal avec des privilèges élevés :
# <a name="cmd"></a>[cmd](#tab/cmd)

```cmd
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\FileSystem]
"LongPathsEnabled"=dword:00000001

```

# <a name="powershell"></a>[PowerShell](#tab/powershell)

```powershell
New-ItemProperty -Path "HKLM:\SYSTEM\CurrentControlSet\Control\FileSystem" `
-Name "LongPathsEnabled" -Value 1 -PropertyType DWORD -Force

```

---

> [!NOTE]  
> Cette clé de Registre peut également être contrôlée via stratégie de groupe à l’adresse `Computer Configuration > Administrative Templates > System > Filesystem > Enable Win32 long paths` .

* Le [manifeste d’application](../sbscs/application-manifests.md) doit également inclure l' `longPathAware` élément.

    ```XML
    <application xmlns="urn:schemas-microsoft-com:asm.v3">
        <windowsSettings xmlns:ws2="http://schemas.microsoft.com/SMI/2016/WindowsSettings">
            <ws2:longPathAware>true</ws2:longPathAware>
        </windowsSettings>
    </application>
    ```

Il s’agit des fonctions de gestion d’annuaire qui n’ont plus de restrictions de **\_ chemin d’accès maximales** si vous optez pour un chemin d’accès long : CreateDirectoryW, CreateDirectoryExW GetCurrentDirectoryW RemoveDirectoryW SetCurrentDirectoryW.

Il s’agit des fonctions de gestion de fichiers qui n’ont plus de restrictions de **\_ chemin d’accès au nombre maximal** si vous optez pour le comportement de chemin d’accès long : CopyFileW, CopyFile2, CopyFileExW, CreateFileW, CreateFile2, CreateHardLinkW, CreateSymbolicLinkW, DeleteFileW, FindFirstFileW, FindFirstFileExW, FindNextFileW, GetFileAttributesW, GetFileAttributesExW, SetFileAttributesW, GetFullPathNameW, GetLongPathNameW, MoveFileW, MoveFileExW, MoveFileWithProgressW, ReplaceFileW, SearchPathW, FindFirstFileNameW
