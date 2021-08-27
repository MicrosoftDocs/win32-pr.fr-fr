---
description: Décrit un jeu complet de valeurs associées à un travail et prend en charge les fichiers de mise en file d’attente volumineux avec des tailles exprimées avec 64 bits.
ms.assetid: 90932ae2-ea9e-43bc-9a1d-c68223f6d0ee
title: Structure JOB_INFO_4 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JOB_INFO_4
- _JOB_INFO_4A
- _JOB_INFO_4W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: dd338b4e6e486c59bfdac705b68c72c56eafb96c9f4e1899e9b4cb3b294791de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120091919"
---
# <a name="job_info_4-structure"></a>\_Structure informations sur le travail \_ 4

Décrit un jeu complet de valeurs associées à un travail et prend en charge les fichiers de mise en file d’attente volumineux avec des tailles exprimées avec 64 bits.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _JOB_INFO_4 {
  DWORD                JobId;
  LPTSTR               pPrinterName;
  LPTSTR               pMachineName;
  LPTSTR               pUserName;
  LPTSTR               pDocument;
  LPTSTR               pNotifyName;
  LPTSTR               pDatatype;
  LPTSTR               pPrintProcessor;
  LPTSTR               pParameters;
  LPTSTR               pDriverName;
  LPDEVMODE            pDevMode;
  LPTSTR               pStatus;
  PSECURITY_DESCRIPTOR pSecurityDescriptor;
  DWORD                Status;
  DWORD                Priority;
  DWORD                Position;
  DWORD                StartTime;
  DWORD                UntilTime;
  DWORD                TotalPages;
  DWORD                Size;
  SYSTEMTIME           Submitted;
  DWORD                Time;
  DWORD                PagesPrinted;
  LONG                 SizeHigh;
} JOB_INFO_4, *PJOB_INFO_4;
```



## <a name="members"></a>Membres

<dl> <dt>

**JobId**
</dt> <dd>

Valeur d’identificateur de tâche.

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

**pNotifyName**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom de l’utilisateur qui doit être averti lorsque le travail a été imprimé ou lorsqu’une erreur se produit lors de l’impression du travail.

</dd> <dt>

**pDatatype**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le type de données utilisé pour enregistrer le travail d’impression.

</dd> <dt>

**pPrintProcessor**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du processeur d’impression qui doit être utilisé pour imprimer le travail.

</dd> <dt>

**pParameters**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie les paramètres du processeur d’impression.

</dd> <dt>

**pDriverName**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du pilote d’imprimante qui doit être utilisé pour traiter le travail d’impression.

</dd> <dt>

**pDevMode**
</dt> <dd>

Pointeur vers une structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) qui contient les données d’initialisation et d’environnement de l’appareil pour le pilote d’imprimante.

</dd> <dt>

**pStatus**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie l’état du travail d’impression. Ce membre doit être vérifié avant l' **État** et, si **PStatus** a la **valeur null**, l’État est défini par le contenu du membre Status.

</dd> <dt>

**pSecurityDescriptor**
</dt> <dd>

La valeur de ce membre est **null**. La récupération et le paramétrage des descripteurs de sécurité de document ne sont pas pris en charge dans cette version.

</dd> <dt>

**État**
</dt> <dd>

État du travail. Ce membre peut être une ou plusieurs des valeurs suivantes :

| Valeur                           | Signification                                                      |
|---------------------------------|--------------------------------------------------------------|
| État du travail \_ \_ bloqué \_ DEVQ      | Le pilote ne peut pas imprimer le travail.                             |
| État du travail \_ \_ supprimé            | La tâche a été supprimée.                                        |
| suppression de l’état du travail \_ \_           | Le travail est en cours de suppression.                                        |
| \_erreur d’état de la tâche \_              | Une erreur est associée au travail.                         |
| État du travail \_ \_ hors connexion            | L’imprimante est hors connexion.                                          |
| \_PAPEROUT État du travail \_           | L’imprimante n’est plus imprimée.                                     |
| État du travail \_ \_ suspendu             | Le travail est suspendu.                                               |
| État du travail \_ \_ imprimé            | Le travail a été imprimé.                                             |
| \_impression de l’état du travail \_           | Le travail est en cours d’impression.                                             |
| redémarrage de l’état du travail \_ \_            | Le travail a été redémarré.                                      |
| mise en file d’attente de l’état du travail \_ \_           | Le travail est en attente.                                             |
| INTERVENTION de l’utilisateur de l’état du travail \_ \_ \_ | L’imprimante a une erreur qui nécessite que l’utilisateur effectue une action. |



 

dans Windows XP et les versions ultérieures de Windows, les valeurs suivantes peuvent également être utilisées :

| Valeur                 | Signification                                                                                       |
|-----------------------|-----------------------------------------------------------------------------------------------|
| État du travail \_ \_ terminé | Le travail est envoyé à l’imprimante, mais il n’est peut-être pas encore imprimé. Pour plus d'informations, consultez la section Notes. |
| État du travail \_ \_ conservé | La tâche a été conservée dans la file d’attente à l’impression après l’impression.                              |



 

</dd> <dt>

**Priorité**
</dt> <dd>

Priorité du travail. Ce membre peut être l’une des valeurs suivantes, ou se trouver dans la plage comprise entre 1 et 99 ( \_ Priorité minimale via \_ priorité maximale).



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

**StartTime**
</dt> <dd>

Heure à laquelle le travail peut être imprimé au plus tôt.

</dd> <dt>

**UntilTime**
</dt> <dd>

Heure à laquelle le travail peut être imprimé au plus tard.

</dd> <dt>

**TotalPages**
</dt> <dd>

Nombre de pages requises pour le travail. Cette valeur peut être égale à zéro si le travail d’impression ne contient pas d’informations de délimitation de page.

</dd> <dt>

**Taille**
</dt> <dd>

Quatre octets inférieurs de la taille, en octets, du travail. Voir aussi le membre **SizeHigh** ci-dessous.

</dd> <dt>

**Envoyée**
</dt> <dd>

Structure [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) qui spécifie l’heure à laquelle le travail a été envoyé.

Cette valeur de date/heure est au format UTC (Universal Time Coordinate). Vous devez la convertir en une valeur d’heure locale avant de l’afficher. Vous pouvez utiliser la fonction [**FileTimeToLocalFileTime**](/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime) pour effectuer la conversion.

</dd> <dt>

**Time**
</dt> <dd>

Durée totale, en millisecondes, qui s’est écoulée depuis le début de l’impression du travail.

</dd> <dt>

**PagesPrinted**
</dt> <dd>

Nombre de pages imprimées. Cette valeur peut être égale à zéro si le travail d’impression ne contient pas d’informations de délimitation de page.

</dd> <dt>

**SizeHigh**
</dt> <dd>

Quatre octets supérieurs de la taille, en octets, du travail. Voir aussi le membre **Size** ci-dessus.

</dd> </dl>

## <a name="remarks"></a>Remarques

Les moniteurs de port qui ne prennent pas en charge TrueEndOfJob définissent le travail en tant qu’État du travail \_ \_ imprimé immédiatement après l’envoi du travail à l’imprimante.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                            |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Winspool. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **\_ \_ Informations sur \_ le travail 4W** (Unicode) et **\_ \_ informations sur le travail \_ 4a** (ANSI)<br/>               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Structures de l’API du spouleur d’impression](printing-and-print-spooler-structures.md)
</dt> <dt>

[**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[**EnumJobs**](enumjobs.md)
</dt> <dt>

[**GetJob**](getjob.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> </dl>

 

