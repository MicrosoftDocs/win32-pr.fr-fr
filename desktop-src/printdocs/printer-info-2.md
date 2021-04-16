---
description: La \_ structure info 2 de l’imprimante \_ spécifie des informations détaillées sur l’imprimante.
ms.assetid: 944cbfcd-9edf-4b60-a45c-9bb1839f8141
title: Structure PRINTER_INFO_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_2
- _PRINTER_INFO_2A
- _PRINTER_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: b299cb1bbdd3ac2475b7a9f2b600bcd9652246d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529757"
---
# <a name="printer_info_2-structure"></a>\_Structure info 2 de l’imprimante \_

La **structure \_ info \_ 2** de l’imprimante spécifie des informations détaillées sur l’imprimante.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _PRINTER_INFO_2 {
  LPTSTR               pServerName;
  LPTSTR               pPrinterName;
  LPTSTR               pShareName;
  LPTSTR               pPortName;
  LPTSTR               pDriverName;
  LPTSTR               pComment;
  LPTSTR               pLocation;
  LPDEVMODE            pDevMode;
  LPTSTR               pSepFile;
  LPTSTR               pPrintProcessor;
  LPTSTR               pDatatype;
  LPTSTR               pParameters;
  PSECURITY_DESCRIPTOR pSecurityDescriptor;
  DWORD                Attributes;
  DWORD                Priority;
  DWORD                DefaultPriority;
  DWORD                StartTime;
  DWORD                UntilTime;
  DWORD                Status;
  DWORD                cJobs;
  DWORD                AveragePPM;
} PRINTER_INFO_2, *PPRINTER_INFO_2;
```



## <a name="members"></a>Membres

<dl> <dt>

**pServerName**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui identifie le serveur qui contrôle l’imprimante. Si cette chaîne est **null**, l’imprimante est contrôlée localement.

</dd> <dt>

**pPrinterName**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom de l’imprimante.

</dd> <dt>

**pShareName**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui identifie le point de partage de l’imprimante. (Cette chaîne est utilisée uniquement si l’imprimante \_ Une \_ constante partagée d’attribut a été définie pour le membre **attributs** .)

</dd> <dt>

**pPortName**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui identifie le ou les ports utilisés pour transmettre des données à l’imprimante. Si une imprimante est connectée à plusieurs ports, les noms de chaque port doivent être séparés par des virgules (par exemple, « LPT1 :, LPT2 :, LPT3 : »).

</dd> <dt>

**pDriverName**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du pilote d’imprimante.

</dd> <dt>

**pComment**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui fournit une brève description de l’imprimante.

</dd> <dt>

**pLocation**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie l’emplacement physique de l’imprimante (par exemple, « Bldg ». 38, salle 1164»).

</dd> <dt>

**pDevMode**
</dt> <dd>

Pointeur vers une structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) qui définit les données d’imprimante par défaut telles que l’orientation du papier et la résolution.

</dd> <dt>

**pSepFile**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du fichier utilisé pour créer la page de séparation. Cette page est utilisée pour séparer les travaux d’impression envoyés à l’imprimante.

</dd> <dt>

**pPrintProcessor**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du processeur d’impression utilisé par l’imprimante. Vous pouvez utiliser la fonction [**EnumPrintProcessors**](enumprintprocessors.md) pour obtenir la liste des processeurs d’impression installés sur un serveur.

</dd> <dt>

**pDatatype**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le type de données utilisé pour enregistrer le travail d’impression. Vous pouvez utiliser la fonction [**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md) pour obtenir la liste des types de données pris en charge par un processeur d’impression spécifique.

</dd> <dt>

**pParameters**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie les paramètres du processeur d’impression par défaut.

</dd> <dt>

**pSecurityDescriptor**
</dt> <dd>

Pointeur vers une structure [**de \_ descripteur de sécurité**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) pour l’imprimante. Ce membre peut avoir la **valeur null**.

</dd> <dt>

**Attributs**
</dt> <dd>

Attributs de l’imprimante. Ce membre peut être une combinaison raisonnable des valeurs suivantes.

| Valeur                                   | Signification                                                                                                                                                                                 |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| attribut d’imprimante \_ \_ direct              | Le travail est envoyé directement à l’imprimante (il n’est pas mis en file d’attente).                                                                                                                                |
| l’attribut d’imprimante se \_ \_ \_ termine en \_ premier | Si l’imprimante est définie et que l’imprimante est définie pour l’impression pendant la mise en file d’attente, toutes les tâches dont l’attente est terminée sont planifiées pour s’imprimer avant les travaux qui n’ont pas terminé la mise en attente.                          |
| attribut d’imprimante \_ \_ Enable \_ DEVQ        | Si cette valeur est définie, **DevQueryPrint** est appelé. **DevQueryPrint** peut échouer si les configurations du document et de l’imprimante ne correspondent pas. La définition de cet indicateur entraîne la conservation des documents incompatibles dans la file d’attente. |
| \_attribut imprimante \_ masqué              | Réservé.                                                                                                                                                                               |
| \_attribut Printer \_ KEEPPRINTEDJOBS     | Si cette valeur est définie, les tâches sont conservées après leur impression. S’il est désactivé, les travaux sont supprimés.                                                                                                               |
| \_attribut imprimante \_ local               | L’imprimante est une imprimante locale.                                                                                                                                                             |
| attribut d’imprimante \_ \_ réseau             | L’imprimante est une connexion d’imprimante réseau.                                                                                                                                                |
| \_attribut Printer \_ publié           | Indique si l’imprimante est publiée dans le service d’annuaire.                                                                                                                    |
| \_attribut d’imprimante en \_ file d’attente              | Si cette valeur est définie, l’imprimante est mise en file d’attente et commence l’impression une fois que la dernière page est mise en file d’attente. Si la valeur n’est pas définie et que \_ l’attribut Printer \_ direct n’est pas défini, l’imprimante met en attente et imprime pendant la mise en attente.      |
| attribut d’imprimante \_ \_ RAW \_ uniquement           | Indique que seuls les travaux d’impression de type de données brutes peuvent être mis en file d’attente.                                                                                                                            |
| attribut d’imprimante \_ \_ partagé              | L’imprimante est partagée.                                                                                                                                                                      |



 

Dans Windows XP et les versions ultérieures de Windows, la valeur suivante peut également être utilisée.

| Valeur                   | Signification                                                                                                                                                                                           |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_télécopie d’attribut d’imprimante \_ | S’il est défini, l’imprimante est une imprimante-télécopieur. Cela ne peut être défini que par [**AddPrinter**](addprinter.md), mais il peut être récupéré par [**EnumPrinters**](enumprinters.md) et [**GetPrinter**](getprinter.md). |



 

Dans Windows Vista et les versions ultérieures de Windows, les valeurs suivantes peuvent également être utilisées.

| Valeur                               | Signification                                                                          |
|-------------------------------------|----------------------------------------------------------------------------------|
| \_ \_ nom convivial de l’attribut d’imprimante \_  | Un ordinateur s’est connecté à cette imprimante et lui a donné un nom convivial.           |
| \_ordinateur d’attribut d’imprimante \_         | L’imprimante est une connexion par ordinateur.                                             |
| attribut d’imprimante \_ \_ Push \_ User    | L’imprimante a été installée à l’aide de la stratégie d’utilisateur envoyer des connexions d’imprimante.     |
| attribut d’imprimante, \_ \_ \_ ordinateur poussé | L’imprimante a été installée à l’aide de la stratégie de l’ordinateur Push Printer Connections. |



 

Dans Windows Server 2003, la valeur suivante peut également être utilisée.

| Valeur                  | Signification                                                                 |
|------------------------|-------------------------------------------------------------------------|
| attribut d’imprimante \_ \_ TS | Indique que l’imprimante est actuellement connectée via un serveur Terminal Server. |



 

</dd> <dt>

**Priorité**
</dt> <dd>

Valeur de priorité que le spouleur utilise pour router les travaux d’impression.

</dd> <dt>

**DefaultPriority**
</dt> <dd>

Valeur de priorité par défaut assignée à chaque travail d’impression.

</dd> <dt>

**StartTime**
</dt> <dd>

Heure à laquelle l’imprimante imprime un travail. Cette valeur est exprimée sous la forme de minutes écoulées depuis 12:00 AM GMT (Greenwich Mean Time).

</dd> <dt>

**UntilTime**
</dt> <dd>

Dernière heure à laquelle l’imprimante imprime un travail. Cette valeur est exprimée sous la forme de minutes écoulées depuis 12:00 AM GMT (Greenwich Mean Time).

</dd> <dt>

**État**
</dt> <dd>

État de l’imprimante. Ce membre peut être une combinaison raisonnable des valeurs suivantes.



| Valeur                               | Signification                                                          |
|-------------------------------------|------------------------------------------------------------------|
| État de l’imprimante \_ \_ occupé               | L'imprimante est occupée.                                             |
| porte de l’état de l’imprimante \_ \_ \_ ouverte         | La porte de l’imprimante est ouverte.                                        |
| \_erreur d’état de l’imprimante \_              | L'imprimante est dans un état d'erreur.                                |
| État de l’imprimante en cours \_ \_ d’initialisation       | L'imprimante s'initialise.                                     |
| \_e/s d’état d’imprimante \_ \_ active         | L’imprimante est dans un état d’entrée/sortie actif                   |
| \_ \_ flux manuel de l’état de l’imprimante \_       | L’imprimante est dans un état de flux manuel.                           |
| État de l’imprimante \_ \_ non \_ toner          | L'imprimante est sans toner.                                     |
| l’état de l’imprimante \_ \_ n’est pas \_ disponible     | L’imprimante n’est pas disponible pour l’impression.                       |
| État de l’imprimante \_ \_ hors connexion            | L'imprimante est hors connexion.                                          |
| \_ \_ mémoire insuffisante sur l’état \_ de \_ l’imprimante    | La mémoire de l’imprimante est insuffisante.                               |
| bac de sortie de l’état de l’imprimante \_ \_ \_ \_ plein  | Le bac de sortie de l'imprimante est plein.                                |
| PAGE État de l’imprimante \_ \_ \_ chargeur         | L’imprimante ne peut pas imprimer la page active.                       |
| \_ \_ bourrage papier sur l’état de l’imprimante \_         | Le papier est coincé dans l’imprimante                                   |
| \_ \_ sortie papier de l’état de l’imprimante \_         | L’imprimante n’est plus imprimée.                                     |
| \_ \_ problème papier sur l’état de l’imprimante \_     | L’imprimante présente un problème de papier.                                 |
| État de l’imprimante \_ \_ suspendu             | L’imprimante est suspendue.                                           |
| État de l’imprimante \_ \_ en attente de \_ suppression  | L’imprimante est en cours de suppression.                                    |
| État de l’imprimante \_ \_ économie d’énergie \_        | L'imprimante est en mode mise en veille.                               |
| \_impression de \_ l’état de l’imprimante           | L’imprimante est en cours d’impression.                                         |
| traitement de l’état de l’imprimante \_ \_         | L’imprimante est en cours de traitement d’un travail d’impression.                           |
| serveur d’état d’imprimante \_ \_ \_ inconnu    | L’état de l’imprimante est inconnu.                                   |
| \_toner d' \_ état \_ faible de l’imprimante         | L’imprimante manque de toner.                                     |
| INTERVENTION de l’utilisateur sur l’état de l’imprimante \_ \_ \_ | L’imprimante a une erreur qui oblige l’utilisateur à effectuer une opération. |
| État de l’imprimante en \_ \_ attente            | L’imprimante est en attente.                                          |
| État de l’imprimante \_ \_ préchauffage \_        | L'imprimante s'allume.                                       |



 

</dd> <dt>

**cJobs**
</dt> <dd>

Nombre de travaux d’impression qui ont été mis en file d’attente pour l’imprimante.

</dd> <dt>

**AveragePPM**
</dt> <dd>

Nombre moyen de pages par minute qui ont été imprimées sur l’imprimante.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **\_ \_ Infos sur \_ l’imprimante 2S** (Unicode) et **\_ \_ infos sur l’imprimante \_ 2A** (ANSI)<br/>                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Structures de l’API du spouleur d’impression](printing-and-print-spooler-structures.md)
</dt> <dt>

[**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[**EnumPrinters**](enumprinters.md)
</dt> <dt>

[**\_Infos sur l’imprimante \_ 1**](printer-info-1.md)
</dt> <dt>

[**\_Infos sur l’imprimante \_ 3**](printer-info-3.md)
</dt> <dt>

[**\_Infos sur l’imprimante \_ 4**](printer-info-4.md)
</dt> <dt>

[**descripteur de sécurité \_**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

 

