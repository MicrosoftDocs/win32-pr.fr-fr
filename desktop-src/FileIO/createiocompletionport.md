---
description: Crée un port de terminaison d’entrée/sortie (e/s) et l’associe à un handle de fichier spécifié, ou crée un port de terminaison d’e/s qui n’est pas encore associé à un descripteur de fichier, ce qui permet une association à un moment ultérieur.
ms.assetid: 40cb47fc-7b15-47f6-bee2-2611d4686053
title: Fonction CreateIoCompletionPort (IoAPI. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateIoCompletionPort
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-io-l1-1-1.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: 6612c3087841aa0c13f131581f8a05c29403e4fccf81bd6f0dc338b1dd9e42a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083159"
---
# <a name="createiocompletionport-function"></a>CreateIoCompletionPort, fonction

Crée un port de terminaison d’entrée/sortie (e/s) et l’associe à un handle de fichier spécifié, ou crée un port de terminaison d’e/s qui n’est pas encore associé à un descripteur de fichier, ce qui permet une association à un moment ultérieur.

L’Association d’une instance d’un descripteur de fichier ouvert à un port de terminaison d’e/s permet à un processus de recevoir une notification de la fin des opérations d’e/s asynchrones impliquant ce descripteur de fichier.

> [!Note]
>
> Le terme *descripteur de fichier* utilisé ici fait référence à une abstraction système qui représente un point de terminaison d’e/s avec chevauchement, et non un fichier sur le disque. Tout objet système qui prend en charge les e/s avec chevauchement, telles que les points de terminaison réseau, les sockets TCP, les canaux nommés et les emplacements de messagerie, peut être utilisé comme descripteurs de fichiers. Pour plus d’informations, consultez la section Notes.

 

## <a name="syntax"></a>Syntaxe


```C++
HANDLE WINAPI CreateIoCompletionPort(
  _In_     HANDLE    FileHandle,
  _In_opt_ HANDLE    ExistingCompletionPort,
  _In_     ULONG_PTR CompletionKey,
  _In_     DWORD     NumberOfConcurrentThreads
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*FileHandle* \[ dans\]
</dt> <dd>

Descripteur de fichier ouvert ou **\_ \_ valeur de handle non valide**.

Le handle doit être un objet qui prend en charge les e/s avec chevauchement.

Si un handle est fourni, il doit avoir été ouvert pour une exécution d’e/s avec chevauchement. Par exemple, vous devez spécifier l’indicateur de **\_ \_ chevauchement** de l’indicateur de fichier lors de l’utilisation de la fonction [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) pour obtenir le descripteur.

Si **une \_ \_ valeur de handle non valide** est spécifiée, la fonction crée un port de terminaison d’e/s sans l’associer à un descripteur de fichier. Dans ce cas, le paramètre *ExistingCompletionPort* doit avoir la **valeur null** et le paramètre *CompletionKey* est ignoré.

</dd> <dt>

*ExistingCompletionPort* \[ dans, facultatif\]
</dt> <dd>

Handle vers un port de terminaison d’e/s existant ou **null**.

Si ce paramètre spécifie un port de terminaison d’e/s existant, la fonction l’associe au handle spécifié par le paramètre *FileHandle* . La fonction retourne le handle du port de terminaison d’e/s existant en cas de réussite ; il ne crée pas de nouveau port de terminaison d’e/s.

Si ce paramètre a la **valeur null**, la fonction crée un nouveau port de terminaison d’e/s et, si le paramètre *FileHandle* est valide, l’associe au nouveau port de terminaison d’e/s. Sinon, aucune association de handles de fichiers ne se produit. En cas de réussite, la fonction retourne le handle au nouveau port de terminaison d’e/s.

</dd> <dt>

*CompletionKey* \[ dans\]
</dt> <dd>

Clé de fin définie par l’utilisateur par handle qui est incluse dans chaque paquet d’achèvement d’e/s pour le handle de fichier spécifié. Pour plus d'informations, consultez la section Notes.

</dd> <dt>

*NumberOfConcurrentThreads* \[ dans\]
</dt> <dd>

Nombre maximal de threads que le système d’exploitation peut autoriser à traiter simultanément les paquets de fin d’exécution d’e/s pour le port de terminaison d’e/s. Ce paramètre est ignoré si le paramètre *ExistingCompletionPort* n’a pas la **valeur null**.

Si ce paramètre est égal à zéro, le système autorise le nombre de threads en cours d’exécution simultanément, car il y a des processeurs dans le système.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction aboutit, la valeur de retour est le descripteur d’un port de terminaison d’e/s :

-   Si le paramètre *ExistingCompletionPort* a la valeur **null**, la valeur de retour est un nouveau handle.

-   Si le paramètre *ExistingCompletionPort* était un handle de port de terminaison d’e/s valide, la valeur de retour est le même handle.

-   Si le paramètre *FileHandle* était un handle valide, ce descripteur de fichier est désormais associé au port de terminaison d’e/s retourné.

Si la fonction échoue, la valeur de retour est **null**. Pour afficher les informations d’erreur étendues, appelez la fonction [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

## <a name="remarks"></a>Remarques

Le système d’e/s peut être invité à envoyer des paquets de notification de fin d’exécution d’e/s aux ports de terminaison d’e/s, où ils sont mis en file d’attente. La fonction **CreateIoCompletionPort** fournit cette fonctionnalité.

Un port de terminaison d’e/s et son descripteur sont associés au processus qui l’a créé et ne peuvent pas être partagés entre les processus. Toutefois, un seul descripteur peut être partagé entre les threads du même processus.

**CreateIoCompletionPort** peut être utilisé dans trois modes distincts :

-   Créez uniquement un port de terminaison d’e/s sans l’associer à un descripteur de fichier.
-   Associer un port de terminaison d’e/s existant à un descripteur de fichier.
-   Effectuez la création et l’Association en un seul appel.

Pour créer un port de terminaison d’e/s sans l’associer, définissez le paramètre *FileHandle* sur **\_ \_ valeur de handle non valide**, le paramètre *ExistingCompletionPort* sur **null** et le paramètre *CompletionKey* sur zéro (ce qui est ignoré dans ce cas). Définissez le paramètre *NumberOfConcurrentThreads* sur la valeur de concurrence souhaitée pour le nouveau port de terminaison d’e/s, ou sur zéro pour la valeur par défaut (le nombre de processeurs dans le système).

Le descripteur passé dans le paramètre *FileHandle* peut être n’importe quel handle qui prend en charge les e/s avec chevauchement. Le plus souvent, il s’agit d’un handle ouvert par la fonction [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) à l’aide de l’indicateur de fichier avec indicateur de **\_ \_ chevauchement** (par exemple, fichiers, emplacements de messagerie et canaux). Les objets créés par d’autres fonctions, tels que [**Socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) , peuvent également être associés à un port de terminaison d’e/s. Pour obtenir un exemple d’utilisation de sockets, consultez la rubrique [**accepted**](/windows/desktop/api/mswsock/nf-mswsock-acceptex). Un descripteur peut être associé à un seul port de terminaison d’e/s et, une fois l’association établie, le handle reste associé à ce port de terminaison d’e/s jusqu’à ce qu’il soit fermé.

Pour plus d’informations sur la théorie, l’utilisation et les fonctions associées du port de terminaison d’e/s, consultez [ports de terminaison d’e/s](i-o-completion-ports.md).

Plusieurs descripteurs de fichiers peuvent être associés à un seul port de terminaison d’e/s en appelant **CreateIoCompletionPort** plusieurs fois avec le même handle de port de terminaison d’e/s dans le paramètre *ExistingCompletionPort* et un autre descripteur de fichier dans le paramètre *FileHandle* à chaque fois.

Utilisez le paramètre *CompletionKey* pour aider votre application à effectuer le suivi des opérations d’e/s terminées. Cette valeur n’est pas utilisée par **CreateIoCompletionPort** pour le contrôle fonctionnel ; au lieu de cela, il est attaché au descripteur de fichier spécifié dans le paramètre *FileHandle* au moment de l’association avec un port de terminaison d’e/s. Cette clé de fin doit être unique pour chaque descripteur de fichier et elle accompagne le descripteur de fichier tout au long du processus de mise en file d’attente d’achèvement interne. Elle est retournée dans l’appel de fonction [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) lorsqu’un paquet de saisie semi-automatique arrive. Le paramètre *CompletionKey* est également utilisé par la fonction [**PostQueuedCompletionStatus**](postqueuedcompletionstatus.md) pour la mise en file d’attente de vos propres paquets d’achèvement à usage spécifique.

Une fois qu’une instance d’un handle ouvert est associée à un port de terminaison d’e/s, elle ne peut pas être utilisée dans la fonction [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) ou [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) , car ces fonctions ont leurs propres mécanismes d’e/s asynchrones.

Il est préférable de ne pas partager un descripteur de fichier associé à un port de terminaison d’e/s en utilisant l’héritage des handles ou un appel à la fonction [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) . Les opérations effectuées avec ces handles en double génèrent des notifications de fin d’exécution. Une attention particulière est conseillée.

Le descripteur de port de terminaison d’e/s et chaque descripteur de fichier associé à ce port de terminaison d’e/s particulier sont appelés *références au port de terminaison d’e/s*. Le port de terminaison d’e/s est libéré lorsqu’il n’y a plus de références à celui-ci. Par conséquent, tous ces handles doivent être correctement fermés pour libérer le port de terminaison d’e/s et les ressources système qui lui sont associées. Une fois ces conditions satisfaites, fermez le handle de port de terminaison d’e/s en appelant la fonction [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) .

dans Windows 8 et Windows Server 2012, cette fonction est prise en charge par les technologies suivantes.



| Technology                                           | Pris en charge      |
|------------------------------------------------------|----------------|
| Protocole SMB (Server Message Block) 3,0<br/>   | Oui<br/> |
| Basculement transparent SMB 3,0 (TFO)<br/>        | Oui<br/> |
| SMB 3,0 avec des partages de fichiers avec montée en puissance parallèle (SO)<br/>   | Oui<br/> |
| Système de fichiers Volume partagé de cluster (CsvFS)<br/> | Oui<br/> |
| Système de fichiers résilient (ReFS)<br/>              | Oui<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP pour applications \[ \| UWP\]<br/>                                                                                                                                                                                                                                                       |
| Serveur minimal pris en charge<br/> | Windows Applications de bureau du serveur 2003 \[ \| applications UWP\]<br/>                                                                                                                                                                                                                                              |
| En-tête<br/>                   | <dl> <dt>IoAPI. h (include Windows. h);</dt> <dt>WinBase. h sur Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 et Windows XP (include Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl>                                                                                                                                                                                                                  |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>                                                                                                                                                                                                                  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Rubriques de présentation**
</dt> <dt>

[Fonctions de gestion de fichiers](file-management-functions.md)
</dt> <dt>

[Ports de terminaison d’e/s](i-o-completion-ports.md)
</dt> <dt>

[utilisation des en-têtes de Windows](/windows/desktop/WinProg/using-the-windows-headers)
</dt> <dt>

[Windows Sockets 2](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

**Fonctions**
</dt> <dt>

[**Accepte**](/windows/desktop/api/mswsock/nf-mswsock-acceptex)
</dt> <dt>

[**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle)
</dt> <dt>

[**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)
</dt> <dt>

[**GetQueuedCompletionStatusEx**](getqueuedcompletionstatusex-func.md)
</dt> <dt>

[**PostQueuedCompletionStatus**](postqueuedcompletionstatus.md)
</dt> <dt>

[**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex)
</dt> <dt>

[**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex)
</dt> </dl>

 

