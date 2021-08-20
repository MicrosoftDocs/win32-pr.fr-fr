---
description: La fonction SetPrinter définit les données pour une imprimante spécifiée ou définit l’état de l’imprimante spécifiée en interrompant l’impression, en reprenant l’impression ou en effaçant tous les travaux d’impression.
ms.assetid: ade367c5-20d6-4da9-bb52-ce6768cf7537
title: SetPrinter, fonction (WinSpool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetPrinter
- SetPrinterA
- SetPrinterW
api_type:
- DllExport
api_location:
- WinSpool.drv
- Ext-MS-Win-printer-WinSpool-l1-1-0.dll
- Ext-MS-Win-printer-WinSpool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: de26915b09cd49e4742b762105d4b9ad4868110e79debfa537c63077d24d1f63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118056151"
---
# <a name="setprinter-function"></a>SetPrinter fonction)

La fonction **SetPrinter** définit les données pour une imprimante spécifiée ou définit l’état de l’imprimante spécifiée en interrompant l’impression, en reprenant l’impression ou en effaçant tous les travaux d’impression.

## <a name="syntax"></a>Syntaxe


```C++
BOOL SetPrinter(
  _In_ HANDLE hPrinter,
  _In_ DWORD  Level,
  _In_ LPBYTE pPrinter,
  _In_ DWORD  Command
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hPrinter* \[ dans\]
</dt> <dd>

Handle vers l’imprimante. Utilisez la fonction [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md)ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.

</dd> <dt>

De *niveau* \[ dans\]
</dt> <dd>

Type de données que la fonction stocke dans la mémoire tampon vers laquelle pointe *pPrinter*. Si le paramètre de *commande* n’est pas égal à zéro, le paramètre de *niveau* doit être égal à zéro.

Cette valeur peut être 0, 2, 3, 4, 5, 6, 7, 8 ou 9.

</dd> <dt>

*pPrinter* \[ dans\]
</dt> <dd>

Pointeur vers une mémoire tampon qui contient les données à définir pour l’imprimante, ou contenant des informations pour la commande spécifiée par le paramètre de *commande* . Le type de données dans la mémoire tampon est déterminé par la valeur de *Level*.



| Niveau                                                                                                | Structure                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**entre**</dt> </dl> | Si le paramètre de *commande* est défini sur l' **\_ \_ \_ État du contrôle d’imprimante**, *pPrinter* doit contenir une valeur **DWORD** qui spécifie le nouvel état de l’imprimante à définir. Pour obtenir la liste des valeurs d’État possibles, consultez le membre **Status** de la structure [**Printer \_ info \_ 2**](printer-info-2.md) . Notez que l’état de l' **imprimante est \_ \_ suspendu** et que la **\_ \_ \_ suppression** de l’état de l’imprimante n’est pas une valeur d’état valide à définir.<br/> Si le *niveau* est 0, mais que le paramètre de *commande* n’est pas l'  État du jeu de contrôle d’imprimante, pPrinter doit avoir la **valeur null**. **\_ \_ \_**<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Structure de l' [**imprimante \_ info \_ 2**](printer-info-2.md) contenant des informations détaillées sur l’imprimante.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | Une structure [**Printer \_ info \_ 3**](printer-info-3.md) contenant les informations de sécurité de l’imprimante.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Une structure [**Printer \_ info \_ 4**](printer-info-4.md) contenant des informations d’imprimante minimales, y compris le nom de l’imprimante, le nom du serveur et si l’imprimante est distante ou locale.<br/>                                                                                                                                                                                                                                                                                                                                         |
| <span id="5"></span><dl> <dt>**5**</dt> </dl> | Une structure [**Printer \_ info \_ 5**](printer-info-5.md) contenant des informations sur l’imprimante, telles que des attributs d’imprimante et des paramètres de délai d’attente.<br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="6"></span><dl> <dt>**6**</dt> </dl> | Une structure [**Printer \_ info \_ 6**](printer-info-6.md) spécifiant la valeur d’état d’une imprimante.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="7"></span><dl> <dt>**7**</dt> </dl> | Structure de l' [**imprimante \_ info \_ 7**](printer-info-7.md) . Le membre *dwAction* de cette structure indique si **SetPrinter** doit publier, annuler la publication, publier à nouveau ou mettre à jour les données de l’imprimante dans le service d’annuaire.<br/>                                                                                                                                                                                                                                                                                                                |
| <span id="8"></span><dl> <dt>**8**</dt> </dl> | Structure [**d' \_ informations \_ d’imprimante 8**](printer-info-8.md) spécifiant les paramètres d’imprimante par défaut globaux.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="9"></span><dl> <dt>**9**</dt> </dl> | Une structure d' [**informations d’imprimante \_ \_ 9**](printer-info-9.md) spécifiant les paramètres d’imprimante par défaut par utilisateur.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

*Commande* \[ dans\]
</dt> <dd>

l’action à effectuer.

Si le paramètre de *niveau* est différent de zéro, définissez la valeur de ce paramètre sur zéro. Dans ce cas, l’imprimante conserve son état actuel et la fonction reconfigure les données de l’imprimante, comme spécifié par les paramètres *Level* et *pPrinter* .

Si le paramètre de *niveau* est égal à zéro, définissez la valeur de ce paramètre sur l’une des valeurs suivantes.



| Valeur                                                                                                                                                                                                  | Signification                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRINTER_CONTROL_PAUSE"></span><span id="printer_control_pause"></span><dl> <dt>**\_pause de contrôle de l’imprimante \_**</dt> </dl>                 | Suspendez l’imprimante.<br/>                                                                                                                       |
| <span id="PRINTER_CONTROL_PURGE"></span><span id="printer_control_purge"></span><dl> <dt>**\_purge du contrôle de l’imprimante \_**</dt> </dl>                 | Supprimer tous les travaux d’impression dans l’imprimante.<br/>                                                                                                    |
| <span id="PRINTER_CONTROL_RESUME"></span><span id="printer_control_resume"></span><dl> <dt>**\_reprise du contrôle de l’imprimante \_**</dt> </dl>              | Reprendre une imprimante suspendue.<br/>                                                                                                                 |
| <span id="PRINTER_CONTROL_SET_STATUS"></span><span id="printer_control_set_status"></span><dl> <dt>**\_État du \_ jeu de contrôle d’imprimante \_**</dt> </dl> | Définissez l’état de l’imprimante.<br/> Définissez le paramètre *pPrinter* sur un pointeur désignant une valeur **DWORD** qui spécifie le nouvel état de l’imprimante.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.

Si la fonction échoue, la valeur de retour est égale à zéro.

Si *Level* a la valeur 7 et que l’action de publication a échoué, **SetPrinter** retourne des **\_ e/s d’erreur \_ en attente** et tente de terminer l’action en arrière-plan. Si le *niveau* est 7 et que l’action de mise à jour a échoué, **SetPrinter** retourne le **fichier d’erreur \_ \_ \_ introuvable**.

## <a name="remarks"></a>Remarques

> [!Note]  
> Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

Vous ne pouvez pas utiliser **SetPrinter** pour modifier l’imprimante par défaut.

Pour modifier les paramètres actuels de l’imprimante, appelez la fonction [**GetPrinter**](getprinter.md) pour récupérer les paramètres actuels dans une structure [**\_ info \_ 2**](printer-info-2.md) de l’imprimante, modifiez les membres de cette structure si nécessaire, puis appelez **SetPrinter**.

La **fonction SetPrinter** ignore les membres **pServerName**, **AveragePPM**, **Status** et **cJobs** d’une structure [**Printer \_ info \_ 2**](printer-info-2.md) .

La suspension d’une imprimante interrompt la planification de tous les travaux d’impression pour cette imprimante, à l’exception du travail d’impression qui peut être en cours d’impression. Les travaux d’impression peuvent être envoyés à une imprimante suspendue, mais aucun travail n’est planifié pour être imprimé sur cette imprimante tant que l’impression n’est pas reprise. Si une imprimante est désactivée, tous les travaux d’impression de cette imprimante sont supprimés, à l’exception du travail d’impression en cours.

Si vous utilisez **SetPrinter** pour modifier la structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) par défaut d’une imprimante (en définissant globalement les valeurs par défaut de l’imprimante), vous devez d’abord appeler la fonction [**DocumentProperties**](documentproperties.md) pour valider la structure **DEVMODE** .

Pour les structures [**Printer \_ info \_ 2**](printer-info-2.md) et [**Printer \_ info \_ 3**](printer-info-3.md) qui contiennent un pointeur vers un descripteur de sécurité, la fonction ne peut définir que les composants du descripteur de sécurité que l’appelant est autorisé à modifier. Pour définir des composants de descripteur de sécurité particuliers, vous devez spécifier les droits d’accès nécessaires lorsque vous appelez la fonction [**OpenPrinter**](openprinter.md) ou [**OpenPrinter2**](openprinter2.md) pour récupérer un handle vers l’imprimante. Le tableau suivant présente les droits d’accès requis pour modifier les différents composants du descripteur de sécurité.



| Autorisation d’accès            | Composant descripteur de sécurité             |
|------------------------------|-------------------------------------------|
| **propriétaire en écriture \_**             | Propriétaire<br/> Groupe principal<br/> |
| **ÉCRITURE \_ DAC**               | Liste de contrôle d’accès discrétionnaire (DACL)  |
| **ACCÉDER à la \_ sécurité du système \_** | Liste de contrôle d’accès système (SACL)         |



 

Si le descripteur de sécurité contient un composant pour lequel l’appelant n’a pas le droit d’accès à modifier, **SetPrinter** échoue. Les composants d’un descripteur de sécurité que vous ne souhaitez pas modifier doivent être **null** ou ne pas être présents, selon le cas. Si vous ne souhaitez pas modifier le descripteur de sécurité et que vous appelez **SetPrinter** avec une structure [**Printer \_ info \_ 2**](printer-info-2.md) , affectez la **valeur null** au membre **pSecurityDescriptor** de cette structure.

Le pare-feu de connexion Internet (ICF) bloque les ports d’imprimante par défaut, mais une exception pour le partage de fichiers et d’imprimantes peut être activée. Si **SetPrinter** est appelé par un administrateur d’ordinateur, il active l’exception. S’il est appelé par un non-administrateur et que l’exception n’a pas déjà été activée, l’appel échoue.

Vous pouvez utiliser le niveau 7 avec la structure de l' [**imprimante \_ info \_ 7**](printer-info-7.md) pour publier, annuler la publication ou mettre à jour les données du service d’annuaire pour l’imprimante. Les données du service d’annuaire pour une imprimante incluent toutes les données stockées sous les \_ \* clés SPLDS par des appels à la fonction [**SetPrinterDataEx**](setprinterdataex.md) pour l’imprimante. Avant d’appeler **SetPrinter**, définissez le membre **pszObjectGUID** de **Printer \_ info \_ 7** sur **null** et définissez le membre *dwAction* sur l’une des valeurs suivantes.



| Valeur                             | Description                                                                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_publication DSPRINT**<br/>   | Publie les données du service d’annuaire.<br/>                                                                                                                                                                                                                                                                                                                                        |
| **\_REpublication DSPRINT**<br/> | Les données du service d’annuaire pour l’imprimante ne sont pas publiées, puis publiées à nouveau, ce qui a pour actualiser toutes les propriétés de l’imprimante publiée. La republication modifie également le GUID de l’imprimante publiée. Utilisez cette valeur si vous pensez que les données publiées de l’imprimante ont été endommagées.<br/>                                                                                         |
| **DSPRINT \_ annuler la publication**<br/> | Annule la publication des données du service d’annuaire.<br/>                                                                                                                                                                                                                                                                                                                                      |
| **\_mise à jour DSPRINT**<br/>    | Met à jour les données du service d’annuaire. C’est identique à la **\_ publication DSPRINT**, à ceci près que **SetPrinter** échoue avec un **fichier d’erreur \_ \_ \_ introuvable** si l’imprimante n’est pas encore publiée.<br/> Utilisez **DSPRINT \_ Update** pour mettre à jour les propriétés publiées, mais ne forcez pas la publication. Les pilotes d’imprimante doivent toujours utiliser la **\_ mise à jour DSPRINT** plutôt que la **\_ publication DSPRINT**.<br/> |



 

**DSPRINT \_ L’instance en attente** n’est pas une valeur *dwAction* valide pour **SetPrinter**.

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>WinSpool. h (inclure Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>WinSpool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>WinSpool. drv</dt> </dl>                   |
| Noms Unicode et ANSI<br/>   | **SetPrinterW** (Unicode) et **SetPrinterA** (ANSI)<br/>                                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinter**](addprinter.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**OpenPrinter2**](openprinter2.md)
</dt> <dt>

[**\_Infos sur l’imprimante \_ 2**](printer-info-2.md)
</dt> <dt>

[**\_Infos sur l’imprimante \_ 3**](printer-info-3.md)
</dt> <dt>

[**\_Infos sur l’imprimante \_ 4**](printer-info-4.md)
</dt> <dt>

[**\_Infos sur l’imprimante \_ 5**](printer-info-5.md)
</dt> <dt>

[**\_Infos sur l’imprimante \_ 6**](printer-info-6.md)
</dt> <dt>

[**\_Infos sur l’imprimante \_ 7**](printer-info-7.md)
</dt> <dt>

[**\_Infos sur l’imprimante \_ 8**](printer-info-8.md)
</dt> <dt>

[**\_Infos sur l’imprimante \_ 9**](printer-info-9.md)
</dt> <dt>

[**SetPrinterDataEx**](setprinterdataex.md)
</dt> </dl>

 

 




