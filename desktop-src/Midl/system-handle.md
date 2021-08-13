---
title: system_handle, attribut
description: L’attribut \ system_handle \ spécifie un type de handle défini par le système.
keywords:
- system_handle MIDL de l’attribut
topic_type:
- apiref
api_name:
- system_handle
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 1cc89818db201f1aca84aa63c6aa49b6b7d9f80b7b6c5e211e724004606c653e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641265"
---
# <a name="system_handle-attribute"></a>system_handle, attribut

L' \[ attribut **system_handle** \] spécifie un type de handle défini par le système qui représente l’accès à un objet système.

``` syntax
[system_handle(system-handle-type[,optional-access-mask])]
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*System-handle-type* 
</dt> <dd>

Spécifie l’une des options de type de handle du système.

Les options valides sont les suivantes :
* [sh_composition](sh-composition.md) : handle de surface DirectComposition
* [sh_event](sh-event.md) -objet d’événement nommé ou sans nom
* [sh_file](sh-file.md) -un fichier ou un périphérique d’e/s
* [sh_job](sh-job.md) -objet de traitement
* [sh_mutex](sh-mutex.md) -un objet mutex nommé ou sans nom
* [sh_pipe](sh-pipe.md) -objet canal nommé ou anonyme
* [sh_process](sh-process.md) -un objet processus
* [sh_reg_key](sh-reg-key.md) -une clé de Registre
* [sh_section](sh-section.md) -une section de mémoire partagée
* [sh_semaphore](sh-semaphore.md) -objet sémaphore nommé ou sans nom
* [sh_socket](sh-socket.md) -objet de socket Winsock
* [sh_thread](sh-thread.md) -objet thread
* [sh_token](sh-token.md) -objet de jeton d’accès

</dd> <dt>

*masque d’accès facultatif*
</dt> <dd>

Demande éventuellement des droits d’accès spécifiques appliqués au descripteur dupliqué. Par défaut, lorsque ce paramètre n’est pas spécifié, le handle est dupliqué avec le même accès. 

Pour spécifier un niveau d’accès différent, utilisez les droits d’accès spécifiques à l’objet correspondant à l’objet système sous-jacent sélectionné.

Pour plus d’informations sur la façon dont les droits d’accès sont propagés au cours de la duplication, consultez la documentation [DuplicateHandle](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .

Des liens vers des listes de droits d’accès pour chaque type d’objet se trouvent dans la référence *DuplicateHandle* , ainsi que dans la page **Voir aussi** les en-têtes de chaque `sh_*` paramètre.

</dd> </dl>

## <a name="remarks"></a>Remarques

Pour pouvoir utiliser cet attribut, l' `-target` indicateur doit avoir la valeur `NT100` (ou une version ultérieure) lors de l’exécution de midl.exe.

Les handles du système sont des handles définis par le système d’exploitation pour fournir l’accès à une ressource système. Le type spécifique de l’objet qui se trouve derrière le descripteur doit être spécifié lors de la déclaration de l’attribut.

Pour un handle marqué `[in]` , le descripteur est dupliqué dans la procédure distante et reste valide pour la durée de cette procédure. Au retour de la procédure distante, le handle dupliqué est libéré. Pour conserver l’accès à l’objet sous-jacent, l’application distante doit dupliquer le handle dans son propre espace d’adressage.

En revanche, pour un handle marqué `[out]` , lorsqu’une procédure distante retourne un descripteur à partir d’un appel, la procédure distante perd la propriété de celle-ci. Pour conserver l’accès à l’objet sous-jacent, la procédure distante doit dupliquer le handle et retourner le doublon. Le handle retourné est alors détenu par l’appelant qui assume la responsabilité de la fermer lorsqu’un accès à l’objet système sous-jacent n’est plus nécessaire.

Comme il s’agit d’un mécanisme de relais d’accès à un objet système, cet attribut s’applique uniquement aux appels entre les procédures sur le même ordinateur.

Les paramètres de création et d’accès donnés à l’objet sous-jacent derrière le descripteur système de sa création déterminent s’il peut être correctement marshalé dans le contexte de procédure distante.

Un tableau de `system_handle` peut être passé dans ou à l’aide de la syntaxe trouvée dans la documentation de l' [**attribut size_is**](size-is.md) .

## <a name="examples"></a>Exemples

Les exemples suivants utilisent plusieurs utilisations de `system_handle` . Pour obtenir un exemple complet, consultez l’exemple [SystemHandlePassing](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SystemHandlePassing) .

```c
interface MyInterface : IUnknown                         
{         
    HRESULT Proc1([in, system_handle(sh_file)] HANDLE writeThisFile);

    HRESULT Proc2([in, system_handle(sh_pipe, FILE_GENERIC_READ)] HANDLE readThisPipe);

    HRESULT Proc3([out, system_handle(sh_composition)] HANDLE* visual);

    HRESULT Proc4([in] DWORD cEvents, [out, system_handle(sh_event), size_is(cEvents)] HANDLE* pWatchAllTheseEvents);
}
```

## <a name="requirements"></a>Configuration requise

| &nbsp; | &nbsp; |
|-|-|
| Client minimal pris en charge | Windows 10 Mise à jour anniversaire (version 1607, Build 14393) |
| Serveur minimal pris en charge | Windows Server 2016 (build 14393) |

## <a name="see-also"></a>Voir aussi

<dl> <dt>
<!--
[System Handle Passing sample code](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SystemHandlePassing)
</dt> <dt>
-->

[/target, commutateur](./-target.md)
</dt> <dt>

[Liaison et Handles](../Rpc/binding-and-handles.md)
</dt> <dt>

[Handles et objets](../sysinfo/handles-and-objects.md)
</dt> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)
</dt> <dt>

[Descripteurs de sécurité](../secauthz/security-descriptors.md)
</dt></dl>
