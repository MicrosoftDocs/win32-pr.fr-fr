---
description: Étant donné que les fichiers sont des objets sécurisables, l’accès à ceux-ci est régi par le modèle de contrôle d’accès qui régit l’accès à tous les autres objets sécurisables dans Windows.
ms.assetid: 991d7d94-fae7-406f-b2e3-dee811279366
title: Sécurité des fichiers et droits d’accès
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c2f33df8117debef1d7f8349ae2fb479974e59ec582d7be758a753726706b9b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696249"
---
# <a name="file-security-and-access-rights"></a>Sécurité des fichiers et droits d’accès

Étant donné que les fichiers sont des [objets sécurisables](/windows/desktop/SecAuthZ/securable-objects), l’accès à ceux-ci est régi par le modèle de contrôle d’accès qui régit l’accès à tous les autres objets sécurisables dans Windows. Pour obtenir une explication détaillée de ce modèle, consultez [Access Control](/windows/desktop/SecAuthZ/access-control).

Vous pouvez spécifier un [descripteur de sécurité](/windows/desktop/api/winnt/ns-winnt-security_descriptor) pour un fichier ou un répertoire lorsque vous appelez la fonction [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea), [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya)ou [**CreateDirectoryEx**](/windows/desktop/api/WinBase/nf-winbase-createdirectoryexa) . Si vous spécifiez **null** pour le paramètre *lpSecurityAttributes* , le fichier ou le répertoire obtient un descripteur de sécurité par défaut. Les listes de contrôle d’accès (ACL) dans le descripteur de sécurité par défaut pour un fichier ou un répertoire sont héritées de son répertoire parent. Notez qu’un descripteur de sécurité par défaut est affecté uniquement lorsqu’un fichier ou un répertoire est nouvellement créé, et non lorsqu’il est renommé ou déplacé.

Pour récupérer le descripteur de sécurité d’un objet de fichier ou de répertoire, appelez la fonction [**GetNamedSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getnamedsecurityinfoa) ou [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) . Pour modifier le descripteur de sécurité d’un objet de fichier ou de répertoire, appelez la fonction [**SetNamedSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setnamedsecurityinfoa) ou [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) .

Les droits d’accès valides pour les fichiers et les répertoires sont les suivants : **supprimer**, lire le contrôle, **écrire \_ DAC**, écrire **\_ le** **\_ propriétaire** et **synchroniser** les [droits d’accès standard](/windows/desktop/SecAuthZ/standard-access-rights). La table dans les [**constantes de droits d’accès aux**](file-access-rights-constants.md) fichiers répertorie les droits d’accès spécifiques aux fichiers et aux répertoires.

Bien que le droit d’accès **Synchronize** soit défini dans la liste des [droits d’accès standard](/windows/desktop/SecAuthZ/standard-access-rights) à la place d’un descripteur de fichier dans une des fonctions Wait, lors de l’utilisation d’opérations d’e/s de fichier asynchrones, vous devez attendre le handle d’événement contenu dans une structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) correctement configurée plutôt que d’utiliser le descripteur de fichier avec le droit d’accès **Synchronize** pour

Vous trouverez ci-dessous les [droits d’accès génériques](/windows/desktop/SecAuthZ/generic-access-rights) pour les fichiers et les répertoires.



<table>
<thead>
<tr class="header">
<th>Droit d’accès</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>FILE_GENERIC_EXECUTE</strong></td>
<td><dl> <strong>FILE_EXECUTE</strong><br />
<strong>FILE_READ_ATTRIBUTES</strong><br />
<strong>STANDARD_RIGHTS_EXECUTE</strong><br />
<strong>NON</strong><br />
</dl></td>
</tr>
<tr class="even">
<td><strong>FILE_GENERIC_READ</strong></td>
<td><dl> <strong>FILE_READ_ATTRIBUTES</strong><br />
<strong>FILE_READ_DATA</strong><br />
<strong>FILE_READ_EA</strong><br />
<strong>STANDARD_RIGHTS_READ</strong><br />
<strong>NON</strong><br />
</dl></td>
</tr>
<tr class="odd">
<td><strong>FILE_GENERIC_WRITE</strong></td>
<td><dl> <strong>FILE_APPEND_DATA</strong><br />
<strong>FILE_WRITE_ATTRIBUTES</strong><br />
<strong>FILE_WRITE_DATA</strong><br />
<strong>FILE_WRITE_EA</strong><br />
<strong>STANDARD_RIGHTS_WRITE</strong><br />
<strong>NON</strong><br />
</dl></td>
</tr>
</tbody>
</table>



 

Windows compare les droits d’accès demandés et les informations contenues dans le jeton d’accès du thread aux informations contenues dans le descripteur de sécurité de l’objet de fichier ou de répertoire. Si la comparaison n’interdit pas l’octroi de tous les droits d’accès demandés, un descripteur de l’objet est renvoyé au thread et les droits d’accès sont accordés. Pour plus d’informations sur ce processus, consultez [interaction entre les threads et les objets sécurisables](/windows/desktop/SecAuthZ/interaction-between-threads-and-securable-objects).

Par défaut, l’autorisation d’accès à un fichier ou à un répertoire est contrôlée exclusivement par les listes de contrôle d’accès dans le descripteur de sécurité associé à ce fichier ou répertoire. En particulier, le descripteur de sécurité d’un répertoire parent n’est pas utilisé pour contrôler l’accès aux fichiers ou répertoires enfants. Le [droit d’accès](/windows/desktop/SecAuthZ/access-rights-and-access-masks) au **\_ parcours du fichier** peut être appliqué en supprimant le [privilège](/windows/desktop/SecAuthZ/privileges) de **contournement du \_ \_ contrôle de parcours** des utilisateurs. Cela n’est pas recommandé dans le cas général, car de nombreux programmes ne gèrent pas correctement les erreurs de traversée de répertoire. L’utilisation principale du droit d’accès au **\_ parcours des fichiers** sur les répertoires consiste à activer la conformité à certaines normes POSIX IEEE et ISO lorsque l’interopérabilité avec les systèmes UNIX est requise.

le modèle de sécurité Windows permet à un répertoire enfant d’hériter d’une ou de plusieurs des entrées du descripteur de sécurité du répertoire parent ou de l’empêcher d’en hériter. Chaque entrée du contrôle d’accès contient des informations qui déterminent la façon dont elle peut être héritée, et si elle a un effet sur l’objet de l’annuaire qui hérite. Par exemple, certaines ACE héritées contrôlent l’accès à l’objet d’annuaire hérité, et celles-ci sont appelées *ACE effectives*. Toutes les autres entrées de du même nom sont appelées *ACE d’héritage uniquement*.

le modèle de sécurité Windows applique également l’héritage automatique des entrées de contrôle d’accès (ace) aux objets enfants en fonction des [règles d’héritage ACE](/windows/desktop/SecAuthZ/ace-inheritance-rules). Cet héritage automatique, ainsi que les informations d’héritage de chaque ACE, déterminent la façon dont les restrictions de sécurité sont transmises dans la hiérarchie de répertoires.

Notez que vous ne pouvez pas utiliser une entrée du contrôle d’accès refusé pour refuser uniquement l’accès **\_ en** **\_ écriture** générique ou générique à un fichier. En effet, pour les objets file, les mappages génériques pour **la \_ lecture générique** ou l' **\_ écriture générique** incluent le droit d’accès **Synchronize** . Si une entrée de contrôle d’accès refuse l’accès en **\_ écriture générique** à un tiers de confiance et que le tiers de confiance demande l’accès **\_ en lecture générique** , la demande échoue, car la demande comprend implicitement l’accès de **synchronisation** qui est implicitement refusé par l’entrée du contrôle d’accès, et vice versa. Au lieu d’utiliser des ACE d’accès refusé, utilisez des ACE access-allowed pour accorder explicitement les droits d’accès autorisés.

Le chiffrement est un autre moyen de gérer l’accès aux objets de stockage. l’implémentation du chiffrement du système de fichiers dans Windows est le système de fichiers chiffré ou EFS. EFS chiffre uniquement les fichiers et non les répertoires. l’avantage du chiffrement est qu’il offre une protection supplémentaire aux fichiers qui sont appliqués sur le support et non par le biais du système de fichiers et de l’architecture de contrôle d’accès Windows standard. Pour plus d’informations sur le chiffrement des fichiers, consultez [chiffrement de fichier](file-encryption.md).

Dans la plupart des cas, la capacité de lire et d’écrire les paramètres de sécurité d’un objet de fichier ou de répertoire est limitée aux processus en mode noyau. En clair, vous ne souhaitez pas que le processus utilisateur soit en mesure de modifier la propriété ou la restriction d’accès sur votre fichier ou Répertoire privé. Toutefois, une application de sauvegarde ne peut pas terminer son travail de sauvegarde de votre fichier si les restrictions d’accès que vous avez placées sur votre fichier ou répertoire n’autorisent pas le processus en mode utilisateur de l’application à le lire. Les applications de sauvegarde doivent être en mesure de remplacer les paramètres de sécurité des objets de fichier et d’annuaire pour garantir une sauvegarde complète. De même, si une application de sauvegarde tente d’écrire une copie de sauvegarde de votre fichier sur la copie résidant sur le disque, et que vous refusez explicitement des privilèges d’écriture au processus de l’application de sauvegarde, l’opération de restauration ne peut pas se terminer. Dans ce cas également, l’application de sauvegarde doit être en mesure de remplacer les paramètres de contrôle d’accès de votre fichier.

les privilèges d’accès **SE \_ \_ nom de sauvegarde** et **SE \_ \_ nom de restauration** ont été créés spécifiquement pour fournir cette possibilité de sauvegarder des applications. Si ces privilèges ont été accordés et activés dans le jeton d’accès du processus d’application de sauvegarde, il peut appeler [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) pour ouvrir votre fichier ou répertoire pour la sauvegarde, en spécifiant le droit d’accès de **\_ contrôle de lecture** standard comme valeur du paramètre *dwDesiredAccess* . Toutefois, pour identifier le processus appelant comme un processus de sauvegarde, l’appel à **CreateFile** doit inclure l’indicateur de sémantique de sauvegarde de l' **\_ indicateur de \_ \_ fichier** dans le paramètre *dwFlagsAndAttributes* . La syntaxe complète de l’appel de fonction est la suivante :


```C++
HANDLE hFile = CreateFile( fileName,                   // lpFileName
                           READ_CONTROL,               // dwDesiredAccess
                           0,                          // dwShareMode
                           NULL,                       // lpSecurityAttributes
                           OPEN_EXISTING,              // dwCreationDisposition
                           FILE_FLAG_BACKUP_SEMANTICS, // dwFlagsAndAttributes
                           NULL );                     // hTemplateFile
```



Cela permettra au processus de l’application de sauvegarde d’ouvrir votre fichier et de remplacer la vérification de sécurité standard. Pour restaurer votre fichier, l’application de sauvegarde utilise la syntaxe d’appel [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) suivante lors de l’ouverture de votre fichier à écrire.


```C++
HANDLE hFile = CreateFile( fileName,                   // lpFileName
                           WRITE_OWNER | WRITE_DAC,    // dwDesiredAccess
                           0,                          // dwShareMode
                           NULL,                       // lpSecurityAttributes
                           CREATE_ALWAYS,              // dwCreationDisposition
                           FILE_FLAG_BACKUP_SEMANTICS, // dwFlagsAndAttributes
                           NULL );                     // hTemplateFile
```



Dans certaines situations, une application de sauvegarde doit être en mesure de modifier les paramètres de contrôle d’accès d’un fichier ou d’un répertoire. C’est le cas, par exemple, lorsque les paramètres de contrôle d’accès de la copie résidant sur le disque d’un fichier ou d’un répertoire sont différents de la copie de sauvegarde. Cela se produit si ces paramètres ont été modifiés après la sauvegarde du fichier ou du répertoire, ou s’ils ont été endommagés.

L’indicateur de la sémantique de sauvegarde de l’indicateur de fichier spécifié dans l’appel à [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) donne au processus d’application de sauvegarde l’autorisation de lire les paramètres de contrôle d’accès du fichier ou du répertoire. **\_ \_ \_** Avec cette autorisation, le processus d’application de sauvegarde peut ensuite appeler [**GetKernelObjectSecurity**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity) et [**SetKernelObjectSecurity**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity) pour lire et réinitialiser les paramètres de contrôle d’accès.

Si une application de sauvegarde doit avoir accès aux [paramètres de contrôle d’accès](/windows/desktop/SecAuthZ/access-control-lists)au niveau système, l’indicateur d’accès de **\_ \_ sécurité système** doit être spécifié dans la valeur de paramètre *dwDesiredAccess* transmise à [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea).

Les applications de sauvegarde appellent [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread) pour lire les fichiers et répertoires spécifiés pour l’opération de restauration, et [**BackupWrite**](/windows/desktop/api/winbase/nf-winbase-backupwrite) pour les écrire.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[droits d’accès standard](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> </dl>

 

 
