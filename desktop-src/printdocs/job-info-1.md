---
description: La \_ structure d’informations sur le travail \_ 1 spécifie les informations de travail d’impression, telles que la valeur de l’identificateur du travail, le nom de l’imprimante pour laquelle le travail est mis en attente, le nom de l’ordinateur qui a créé le travail d’impression, le nom de l’utilisateur propriétaire du travail d’impression, et ainsi de suite.
ms.assetid: d42ada89-6bc7-4006-81d9-dbcc0347edd3
title: Structure JOB_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JOB_INFO_1
- _JOB_INFO_1A
- _JOB_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: d56d4d6bce15a661ce141d8e22d27a15837a9f6f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127519480"
---
# <a name="job_info_1-structure"></a>\_Structure informations sur le travail \_ 1

La structure d’informations **sur le travail \_ \_ 1** spécifie les informations de travail d’impression, telles que la valeur de l’identificateur du travail, le nom de l’imprimante pour laquelle le travail est mis en attente, le nom de l’ordinateur qui a créé le travail d’impression, le nom de l’utilisateur propriétaire du travail d’impression, et ainsi de suite.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _JOB_INFO_1 {
  DWORD      JobId;
  LPTSTR     pPrinterName;
  LPTSTR     pMachineName;
  LPTSTR     pUserName;
  LPTSTR     pDocument;
  LPTSTR     pDatatype;
  LPTSTR     pStatus;
  DWORD      Status;
  DWORD      Priority;
  DWORD      Position;
  DWORD      TotalPages;
  DWORD      PagesPrinted;
  SYSTEMTIME Submitted;
} JOB_INFO_1, *PJOB_INFO_1;
```



## <a name="members"></a>Membres

<dl> <dt>

**JobId**
</dt> <dd>

Identificateur de tâche.

</dd> <dt>

**pPrinterName**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom de l’imprimante pour laquelle le travail est mis en attente.

</dd> <dt>

**pMachineName**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom de l’ordinateur qui a créé le travail d’impression.

</dd> <dt>

**pUserName**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom de l’utilisateur propriétaire du travail d’impression.

</dd> <dt>

**pDocument**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du travail d’impression (par exemple, "MS-WORD : Review.doc").

</dd> <dt>

**pDatatype**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le type de données utilisé pour enregistrer le travail d’impression.

</dd> <dt>

**pStatus**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie l’état du travail d’impression. Ce membre doit être vérifié avant l' *État* et, si *PStatus* a la **valeur null**, l’État est défini par le contenu du membre Status.

</dd> <dt>

**État**
</dt> <dd>

État du travail. La valeur de ce membre peut être zéro ou une combinaison d’une ou plusieurs des valeurs suivantes. La valeur zéro indique que la file d’attente à l’impression a été suspendue après la fin de la mise en attente du document.



| Valeur                           | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| État du travail \_ \_ bloqué \_ DEVQ      | Le pilote ne peut pas imprimer le travail.                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| État du travail \_ \_ terminé           | **Windows XP et versions ultérieures :** Le travail est envoyé à l’imprimante, mais le travail n’est peut-être pas encore imprimé.<br/> Pour plus d'informations, consultez la section Notes.<br/>                                                                                                                                                                                                                                                                                                                           |
| État du travail \_ \_ supprimé            | La tâche a été supprimée.                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| suppression de l’état du travail \_ \_           | Le travail est en cours de suppression.                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| \_erreur d’état de la tâche \_              | Une erreur est associée au travail.                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| État du travail \_ \_ hors connexion            | L’imprimante est hors connexion.                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| \_PAPEROUT État du travail \_           | L’imprimante n’est plus imprimée.                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| État du travail \_ \_ suspendu             | Le travail est suspendu.                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| État du travail \_ \_ imprimé            | Le travail a été imprimé.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| \_impression de l’état du travail \_           | Le travail est en cours d’impression.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| redémarrage de l’état du travail \_ \_            | Le travail a été redémarré.                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| État du travail \_ \_ conservé           | **Windows Vista et versions ultérieures :** La tâche a été conservée dans la file d’attente à l’impression et ne peut pas être supprimée. Ceci peut être lié aux problèmes suivants :<br/> 1) la tâche a été conservée manuellement par un appel à SetJob et le spouleur attend que la tâche soit libérée.<br/> 2) le travail n’a pas terminé l’impression et doit terminer l’impression avant de pouvoir être supprimé automatiquement.<br/> Pour plus d’informations sur les commandes de travail d’impression, consultez [**SetJob**](setjob.md) .<br/> |
| mise en file d’attente de l’état du travail \_ \_           | Le travail est en attente.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| INTERVENTION de l’utilisateur de l’état du travail \_ \_ \_ | L’imprimante a une erreur qui nécessite que l’utilisateur effectue une action.                                                                                                                                                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

**Priorité**
</dt> <dd>

Priorité du travail. Ce membre peut être l’une des valeurs suivantes ou se trouver dans la plage comprise entre 1 et 99 ( \_ Priorité minimale via \_ priorité maximale).



| Valeur         | Signification           |
|---------------|-------------------|
| priorité MIN. \_ | Priorité minimale. |
| priorité MAX. \_ | Priorité maximale. |
| priorité de définition \_ | Priorité par défaut. |



 

</dd> <dt>

**Position**
</dt> <dd>

Position du travail dans la file d’attente à l’impression.

</dd> <dt>

**TotalPages**
</dt> <dd>

Nombre total de pages contenues dans le document. Cette valeur peut être égale à zéro si le travail d’impression ne contient pas d’informations de délimitation de page.

</dd> <dt>

**PagesPrinted**
</dt> <dd>

Nombre de pages imprimées. Cette valeur peut être égale à zéro si le travail d’impression ne contient pas d’informations de délimitation de page.

</dd> <dt>

**Envoyée**
</dt> <dd>

Structure [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) qui spécifie l’heure à laquelle ce document a été mis en file d’attente.

Cette valeur de date/heure est au format UTC (Universal Time Coordinate). Vous devez la convertir en une valeur d’heure locale avant de l’afficher. Vous pouvez utiliser la fonction [**FileTimeToLocalFileTime**](/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime) pour effectuer la conversion.

</dd> </dl>

## <a name="remarks"></a>Notes

Les moniteurs de port qui ne prennent pas en charge TrueEndOfJob définissent le travail en tant qu’État du travail \_ \_ imprimé juste après l’envoi du travail à l’imprimante.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **\_ \_ Informations sur \_ les travaux 1s** (Unicode) et **\_ \_ informations sur les travaux \_ 1a** (ANSI)<br/>                                   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Structures de l’API du spouleur d’impression](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumJobs**](enumjobs.md)
</dt> <dt>

[**GetJob**](getjob.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> </dl>

 

