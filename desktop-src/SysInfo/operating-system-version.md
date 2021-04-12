---
description: Les fonctions d’assistance de l’API de version sont utilisées pour déterminer la version du système d’exploitation en cours d’exécution. Pour plus d’informations, consultez obtention de la version du système.
ms.assetid: 1a70b1d9-ed66-4201-9921-4e26e4001020
title: Version du système d'exploitation
ms.topic: article
ms.date: 09/15/2020
ms.openlocfilehash: 73eb9a81880f29f9292713af46c5c79a7e9eb2de
ms.sourcegitcommit: 7ea69db68bca2b1592802e676ada8432a2583410
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/17/2020
ms.locfileid: "104032039"
---
# <a name="operating-system-version"></a>Version du système d'exploitation

Les [fonctions d’assistance](version-helper-apis.md) de l’API de version sont utilisées pour déterminer la version du système d’exploitation en cours d’exécution. Pour plus d’informations, consultez [obtention de la version du système](getting-the-system-version.md).

Le tableau suivant récapitule les numéros de version des systèmes d’exploitation les plus récents.

| Système d’exploitation | Numéro de version |
|------------------|----------------|
| Windows 10       | 10,0\*         |
| Windows Server 2019 | 10,0\*      |
| Windows Server 2016 | 10,0\*      |
| Windows 8.1      | 6.3\*          |
| Windows Server 2012 R2 | 6.3\*    |
| Windows 8        | 6.2            |
| Windows Server 2012 | 6.2         |
| Windows 7        | 6.1            |
| Windows Server 2008 R2 | 6.1      |
| Windows Server 2008 | 6.0         |
| Windows Vista    | 6.0            |
| Windows Server 2003 R2 | 5.2      |
| Windows Server 2003 | 5.2         |
| Windows XP Édition 64 bits | 5.2   |
| Windows XP | 5,1                  |
| Windows 2000     | 5.0            |

**\*** Pour les applications qui ont été manifestées pour Windows 8.1 ou Windows 10. Les applications qui ne sont pas manifestes pour Windows 8.1 ou Windows 10 retournent la valeur de version du système d’exploitation Windows 8 (6,2). Pour manifester vos applications pour Windows 8.1 ou Windows 10, reportez-vous à [ciblage de votre application pour Windows](targeting-your-application-at-windows-8-1.md).<br/>

L’identification du système d’exploitation actuel n’est généralement pas la meilleure façon de déterminer si une fonctionnalité particulière du système d’exploitation est présente. Cela est dû au fait que de nouvelles fonctionnalités ont été ajoutées au système d’exploitation dans une DLL redistribuable. Au lieu d’utiliser les fonctions d’assistance de l' [API de version](version-helper-apis.md) pour déterminer la plate-forme ou le numéro de version du système d’exploitation, vérifiez la présence de la fonctionnalité elle-même.

Pour déterminer la meilleure façon de tester une fonctionnalité, reportez-vous à la documentation de la fonctionnalité qui vous intéresse. La liste suivante présente quelques techniques courantes pour la détection de fonctionnalités :

- Vous pouvez tester la présence des fonctions associées à une fonctionnalité. Pour tester la présence d’une fonction dans une DLL système, appelez la fonction [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) pour charger la dll. Appelez ensuite la fonction [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) pour déterminer si la fonction d’intérêt est présente dans la dll. Utilisez le pointeur retourné par **GetProcAddress** pour appeler la fonction. Notez que même si la fonction est présente, il peut s’agir d’un stub qui retourne simplement un code d’erreur tel que l’appel d’erreur \_ \_ non \_ implémenté.
- Vous pouvez déterminer la présence de certaines fonctionnalités à l’aide de la fonction [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) . Par exemple, vous pouvez détecter plusieurs moniteurs d’affichage en appelant **GetSystemMetrics**(SM \_ CMONITORS).
- Il existe plusieurs versions des dll redistribuables qui implémentent l’interpréteur de commandes et les fonctionnalités de contrôle communes. Pour plus d’informations sur la détermination des versions présentes sur le système sur lequel votre application s’exécute, consultez la rubrique [Shell et versions des contrôles communs](/previous-versions/windows/desktop/legacy/bb776779(v=vs.85)).

Si vous devez exiger un système d’exploitation particulier, veillez à l’utiliser comme version minimale prise en charge, plutôt que de concevoir le test pour l’un des systèmes d’exploitation. De cette façon, votre code de détection continuera à fonctionner sur les futures versions de Windows.

Notez qu’une application 32 bits peut détecter si elle s’exécute sous WOW64 en appelant la fonction [**IsWow64Process**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process) . Il peut obtenir des informations supplémentaires sur le processeur en appelant la fonction [**GetNativeSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getnativesysteminfo) .

Pour plus d’informations, consultez [informations sur la version Windows 10](/windows/release-information/) et [feuille de faits du cycle de vie Windows](https://support.microsoft.com/help/13853/windows-lifecycle-fact-sheet).

