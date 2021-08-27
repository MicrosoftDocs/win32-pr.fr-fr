---
title: Clés de Registre affectées par WOW64
description: Sous WOW64, certaines clés de Registre sont redirigées.
ms.assetid: 7b3f4f11-24bc-44f7-837e-d61d853c7291
keywords:
- clés de registre 64-bit Windows programmation
- Windows de la programmation WOW64 64 bits, clés de registre
- clés de registre redirigées 64 bits Windows programmation
- clés de registre réfléchies 64 bits Windows programmation
- clés de registre partagées 64 bits Windows programmation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5193d4aa64848d132aca446c6d1e4a50777614725b69cae637da65aebfe94c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071609"
---
# <a name="registry-keys-affected-by-windows-installations-that-include-windows-on-windows-wow-support-for-multiple-processor-architectures"></a>clés de registre affectées par les Installations Windows qui incluent la prise en charge de Windows sur Windows (WOW) pour plusieurs architectures de processeur

dans les installations de Windows bits 64 à partir de Windows XP et Windows Server 2003, et dans une architecture de processeur ARM 32 bits Windows installations commençant par Windows RT (Windows 8) (ci-après, les **installations Windows affectées**), certaines clés de registre sont *redirigées*.

sur les installations de Windows concernées, lorsqu’un processus avec une architecture de processeur différente de l’architecture de processeur du système d’exploitation (appelé ci-après comme **application WOW**) effectue un appel de registre pour une clé redirigée, le redirecteur de registre intercepte l’appel et le mappe à l’emplacement physique correspondant du registre de la clé. par exemple, une application intel IA-32 x86 32 bits \[  \] s’exécutant sur une installation Windows **AMD64** /intel x86-x64 est affectée par une clé de registre redirigée ; lorsque cette application x86 appelle une clé redirigée, le redirecteur du registre intercepte l’appel de l’application et le redirige vers l’emplacement physique correspondant du registre de la clé. Pour plus d’informations, consultez [redirecteur du Registre](registry-redirector.md).

d’autres clés de registre sont *partagées* par les applications d’architectures de processeur différentes sur les installations de Windows affectées. Les appels du registre de l’application WOW aux clés partagées ne sont pas redirigés. Au lieu de cela, une copie physique de la clé est mappée à chaque vue logique du Registre.

**Windows server 2008, Windows Vista, Windows server 2003 et Windows XP :** Un sous-ensemble de clés de Registre redirigées est également *reflété* pour conserver les clés et leurs valeurs synchronisées entre les vues 32 bits et 64 bits du Registre. la réflexion du registre a été supprimée à partir de Windows 7 et Windows Server 2008 R2. Pour plus d’informations, consultez [Registry Reflection](registry-reflection.md).

Cette rubrique répertorie les clés de Registre qui sont redirigées, partagées ou redirigées et reflétées sous WOW. elle répertorie également les liens symboliques qui assurent la compatibilité pour les applications existantes qui peuvent utiliser des chemins d’accès de clé de registre codés en dur contenant **Wow6432Node**, l’emplacement de registre redirigé pour les processus x86 s’exécutant sur des installations Windows AMD64. Pour plus d’informations, consultez les rubriques suivantes :

- [Clés redirigées, partagées et reflétées sous WOW](#redirected-shared-and-reflected-keys-under-wow)
- [Windows les liens symboliques de Windows 64 (WOW64)](#windows-on-windows-64-wow64-symbolic-links)

## <a name="redirected-shared-and-reflected-keys-under-wow"></a>Clés redirigées, partagées et reflétées sous WOW

pour les applications WOW sur les installations de Windows concernées, le tableau suivant répertorie les clés de registre qui sont redirigées, partagées, redirigées et reflétées. Les sous-clés des clés de ce tableau héritent du comportement de la clé parent, sauf indication contraire. Si une clé n’a pas de parent listé dans ce tableau, la clé est partagée.

| Clé | Windows Server 2008 R2, Windows 7 et versions ultérieures | Windows Server 2008, Windows Vista, Windows Server 2003 et Windows XP |
|-|-|-|
| **HKEY \_ local \_ machine** | Partagé | Partagé |
| **HKEY \_ local \_ MACHINE\SOFTWARE** | Redirected | Redirected |
| **HKEY \_ Classes \_ MACHINE\SOFTWARE locales** \\  | Partagé | Redirigé et reflété |
| **HKEY \_ AppID local \_ MACHINE\SOFTWARE** \\ **classes** \\ **AppID** | Partagé | Redirigé et reflété avec une exception : les valeurs de Registre [DllSurrogate](../com/dllsurrogate.md) et [DllSurrogateExecutable]( ../com/dllsurrogateexecutable.md) ne sont pas reflétées si leur valeur est une chaîne vide. |
| **HKEY \_ \_** CLSID des \\  \\ **classes** \\  logicielles de l’ordinateur local | Redirected | Redirigé et reflété uniquement pour les CLSID qui ne spécifient pas InprocServer32 ou InprocHandler32. |
| **HKEY \_ \_** \\ **Classes logicielles** de l’ordinateur LOCAL \\  \\ **DirectShow** | Redirected | Redirigé et reflété |
| **HKEY \_ \_** Classes de logiciels de l’ordinateur local \\  \\  \\ **HCP** | Partagé | Partagé |
| **HKEY \_ \_** Interface des \\  \\ **classes** \\  de logiciels de l’ordinateur local | Redirected | Redirigé et reflété |
| **HKEY \_ \_** Type de \\  \\ **média** des classes MACHINE\SOFTWARE locales | Redirected | Redirigé et reflété |
| **HKEY \_ \_** \\ **Classes logicielles** de l’ordinateur local \\  \\ **MediaFoundation** | Redirected | Redirigé et reflété |
| **HKEY \_ \_** Clients de \\ **logiciels** \\  d’ordinateur local | Partagé | Redirected |
| **HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **COM3** | Partagé | Redirigé et reflété |
| **HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **Cryptography** \\ **Calais** \\ **actuel** | Partagé | Partagé |
| **HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **Cryptography** \\ **Calais** \\ **Readers** | Partagé | Partagé |
| **HKEY \_ \_** Services de \\  \\  \\ **chiffrement** \\  Microsoft du logiciel de l’ordinateur local | Partagé | Partagé |
| **HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **CTF** \\ **SystemShared** | Partagé | Partagé |
| **HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **CTF** \\ **Tip** | Partagé | Partagé |
| **HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **DFS** | Partagé | Partagé |
| **HKEY \_ \_** Signature du \\  \\  \\ **pilote** Microsoft du logiciel de l’ordinateur local | Partagé | Partagé |
| **HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **EnterpriseCertificates** | Partagé | Partagé |
| **HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **EventSystem** | Partagé | Redirigé et reflété |
| **HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **MSMQ** | Partagé | Partagé |
| **HKEY \_ Signature \_** du logiciel de l’ordinateur local \\  \\ **Microsoft** \\ **non-Driver** | Partagé | Partagé |
| **HKEY \_ logiciel de l' \_ ordinateur LOCAL** \\  \\ **Microsoft** \\ **Bloc-notes** \\ **DefaultFonts** | Partagé | Redirected |
| **HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **OLE** | Partagé | Redirigé et reflété |
| **HKEY \_ Logiciel d' \_ ordinateur local** \\  \\ **Microsoft** \\ **RAS** | Partagé | Partagé |
| **HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **RPC** | Partagé | Redirigé et reflété |
| **HKEY \_ \_Ordinateur local** \\ **logiciel** \\ **Microsoft** \\ **Microsoft** \\  \\ **Shared Tools** \\ **MSInfo** | Partagé | Partagé |
| **HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **SystemCertificates** | Partagé | Partagé |
| **HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **TermServLicensing** | Partagé | Partagé |
| **HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **TransactionServer** | Partagé | Partagé |
| **HKEY \_ logiciel de l' \_ ordinateur LOCAL** \\  \\ **Microsoft** \\ **Windows** les \\  \\ **chemins d’accès** de l’application CurrentVersion | Partagé | Redirected |
| **HKEY \_ logiciel de l' \_ ordinateur LOCAL** \\  \\ **Microsoft** \\ **Windows** \\  \\ **le panneau de configuration** CurrentVersion \\  \\ **schémas** de curseur | Partagé | Partagé |
| **HKEY \_ logiciel de l' \_ ordinateur LOCAL** \\  \\ **Microsoft** \\ **Windows** l' \\  \\ **explorateur** CurrentVersion \\ **AutoplayHandlers** | Partagé | Redirected |
| **HKEY \_ logiciel de l' \_ ordinateur LOCAL** \\  \\ **Microsoft** \\ **Windows** l' \\  \\ **explorateur** CurrentVersion \\ **DriveIcons** | Partagé | Redirected |
| **HKEY \_ logiciel de l' \_ ordinateur LOCAL** \\  \\ **Microsoft** \\ **Windows** l' \\  \\ **explorateur** CurrentVersion \\ **KindMap** | Partagé | Redirected |
| **HKEY \_ logiciel de l' \_ ordinateur LOCAL** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **stratégie de groupe** | Partagé | Partagé |
| **HKEY \_ logiciel de l' \_ ordinateur LOCAL** \\  \\ **Microsoft** \\ **Windows** \\  \\ **stratégies** CurrentVersion | Partagé | Partagé |
| **HKEY \_ logiciel de l' \_ ordinateur LOCAL** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **PreviewHandlers** | Partagé | Redirected |
| **HKEY \_ logiciel de l' \_ ordinateur LOCAL** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Setup** | Partagé | Partagé |
| **HKEY \_ logiciel de l' \_ ordinateur LOCAL** \\  \\ **Microsoft** \\ **Windows** les \\  \\  \\ **emplacements** de téléphonie CurrentVersion | Partagé | Partagé |
| **HKEY \_ Console \_** du logiciel de l’ordinateur LOCAL \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Console**| Partagé | Redirected |
| **HKEY \_ logiciel de l' \_ ordinateur LOCAL** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **FontDpi** | Partagé | Partagé |
| **HKEY \_ logiciel de l' \_ ordinateur LOCAL** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **FontLink** | Partagé | Redirected |
| **HKEY \_ logiciel de l' \_ ordinateur LOCAL** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **FontMapper** | Partagé | Partagé |
| **HKEY \_ logiciel de l' \_ ordinateur LOCAL** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **polices** | Partagé | Partagé |
| **HKEY \_ logiciel de l' \_ ordinateur LOCAL** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **FontSubstitutes** | Partagé | Partagé |
| **HKEY \_ logiciel de l' \_ ordinateur LOCAL** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Gre \_ initialize** | Partagé | Redirected |
| **HKEY \_ logiciel de l' \_ ordinateur LOCAL** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Image File Execution Options** | Partagé | Redirected |
| **HKEY \_ logiciel de l' \_ ordinateur LOCAL** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Language Pack** | Partagé | Redirected |
| **HKEY \_ logiciel de l' \_ ordinateur LOCAL** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **NetworkCards** | Partagé | Partagé |
| **HKEY \_ logiciel de l' \_ ordinateur LOCAL** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Perflib** | Partagé | Partagé |
| **HKEY \_ logiciel de l' \_ ordinateur LOCAL** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Ports** | Partagé | Partagé |
| **HKEY \_ logiciel de l' \_ ordinateur LOCAL** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Print** | Partagé | Partagé |
| **HKEY \_ logiciel de l' \_ ordinateur LOCAL** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **ProfileList** | Partagé | Partagé |
| **HKEY \_ logiciel de l' \_ ordinateur LOCAL** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **fuseaux horaires** | Partagé | Partagé |
| **HKEY \_ \_** \\ **Stratégies logicielles** \\  de l’ordinateur local | Partagé | Partagé |
| **HKEY \_ \_** \\  \\ **RegisteredApplications** logiciel de l’ordinateur local | Partagé | Partagé **Windows Server 2003 et Windows XP :** cette clé a été ajoutée dans Windows Vista. |
| **HKEY \_ Current \_ User** | Partagé | Partagé |
| **HKEY \_ logiciel \_ utilisateur actuel** \\  | Partagé | Partagé |
| **HKEY \_ \_** \\ **Classes logicielles** \\  de l’utilisateur actuel | Partagé | Redirigé et reflété |
| **HKEY \_ Classes de logiciels \_ utilisateur actuelles** \\  \\  \\ **AppID** | Partagé | Redirigé et reflété avec une exception : les valeurs de Registre [DllSurrogate](../com/dllsurrogate.md) et [DllSurrogateExecutable]( ../com/dllsurrogateexecutable.md) ne sont pas reflétées si leur valeur est une chaîne vide. |
| **HKEY \_ \_** CLSID des \\  \\ **classes** \\  logicielles de l’utilisateur actuel | Redirected | Redirigé et reflété |
| **HKEY \_ Classes de logiciels \_ utilisateur actuelles** \\  \\  \\ **DirectShow** | Redirected | Redirigé et reflété |
| **HKEY \_ \_** Interface des \\  \\ **classes** \\  logicielles de l’utilisateur actuel | Redirected | Redirigé et reflété |
| **HKEY \_ \_** Type de \\  \\  \\ **média** des classes logicielles de l’utilisateur actuel | Redirected | Redirigé et reflété |
| **HKEY \_ \_** \\ **Classes logicielles** de l’utilisateur actuel \\  \\ **MediaFoundation** | Redirected | Redirigé et reflété |

**HKEY \_ L' \_ utilisateur actuel** est un lien symbolique vers le SID **\_** \\ **\[ \]** de HKEY Users où \[ sid \] indique une correspondance pour l’ID de sécurité (SID) de l’utilisateur actuel. **HKEY \_ Les** \\ classes de logiciels **\[ \] sid** des utilisateurs \\  \\  sont un lien symbolique vers les **\_** \\ **\[ \] \_ classes sid** de HKEY Users.

**HKEY \_ La \_ racine des classes** est une vue fusionnée des classes de logiciels de l' **\_ \_ ordinateur local HKEY** \\  \\  et des classes de logiciels de **HKEY \_ Current \_ User** \\  \\ . Les clés redirigées dans ces chemins de Registre sont effectivement redirigées pour la **\_ \_ racine des classes HKEY** également. Cela est également vrai pour les clés reflétées sur les systèmes qui les prennent en charge.

## <a name="windows-on-windows-64-wow64-symbolic-links"></a>Windows les liens symboliques de Windows 64 (WOW64)

WOW64 définit les liens symboliques suivants uniquement pour la compatibilité avec les applications existantes qui peuvent utiliser des chemins d’accès de clé de Registre codés en dur contenant Wow6432Node. Les nouvelles applications doivent éviter d’utiliser Wow6432Node dans les chemins d’accès des clés de registre.

- **HKEY \_ Les \_ \\ \\ \\ Classes Wow6432Node logicielles de l’ordinateur local** sont liées à **HKEY \_ local \_ machine \\ classes logicielles \\ \\ Wow6432Node**
- **HKEY \_ Les \_ classes de logiciels de l’ordinateur local \\ \\ \\ Wow6432Node \\ AppID** sont liées à **HKEY \_ local \_ machine \\ Software \\ classes \\ AppID**
- **HKEY \_ Classes de logiciels de l’ordinateur LOCAL les \_ \\ \\ \\ \\ protocoles Wow6432Node** sont liés à **HKEY \_ local \_ machine \\ classes logicielles \\ \\ protocoles**
- **HKEY \_ Les \_ classes de logiciels de l’ordinateur local \\ \\ \\ Wow6432Node \\ TypeLib** sont liées à **HKEY \_ local \_ machine \\ Software \\ classes \\ TypeLib**

**Windows server 2008, Windows Vista, Windows Server 2003 et Windows XP : HKEY \_ Les \_ \\ \\ \\ Classes Wow6432Node logicielles de l’ordinateur local** sont liées à **HKEY \_ local \_ machine \\ classes logicielles \\ \\ Wow6432Node**. d’autres liens symboliques ont été ajoutés à Windows 7 et Windows Server 2008 R2.
