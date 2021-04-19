---
description: La fonction GetPrinter récupère des informations sur une imprimante spécifiée.
ms.assetid: f162edbb-83ee-40c3-8710-9c867301d652
title: GetPrinter, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinter
- GetPrinterA
- GetPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-0.dll
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: e99b3574762b84b830845da8149b0406664b6da7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523420"
---
# <a name="getprinter-function"></a>GetPrinter fonction)

La fonction **GetPrinter** récupère des informations sur une imprimante spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
BOOL GetPrinter(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPrinter,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hPrinter* \[ dans\]
</dt> <dd>

Handle vers l’imprimante pour laquelle la fonction récupère des informations. Utilisez la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.

</dd> <dt>

De *niveau* \[ dans\]
</dt> <dd>

Niveau ou type de structure que la fonction stocke dans la mémoire tampon vers laquelle pointe *pPrinter*.

Cette valeur peut être 1, 2, 3, 4, 5, 6, 7, 8 ou 9.

</dd> <dt>

*pPrinter* \[ à\]
</dt> <dd>

Pointeur vers une mémoire tampon qui reçoit une structure contenant des informations sur l’imprimante spécifiée. La mémoire tampon doit être suffisamment grande pour recevoir la structure et toutes les chaînes ou autres données auxquelles les membres de la structure pointent. Si la mémoire tampon est trop petite, le paramètre *pcbNeeded* retourne la taille de mémoire tampon requise.

Le type de structure est déterminé par la valeur de *Level*.



| Level                                                                                                | Structure                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Une structure d’informations d' [**imprimante \_ \_ 1**](printer-info-1.md) contenant des informations générales sur l’imprimante.<br/>                                                                                                        |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Structure de l' [**imprimante \_ info \_ 2**](printer-info-2.md) contenant des informations détaillées sur l’imprimante.<br/>                                                                                             |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | Une structure [**Printer \_ info \_ 3**](printer-info-3.md) contenant les informations de sécurité de l’imprimante.<br/>                                                                                                 |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Une structure [**Printer \_ info \_ 4**](printer-info-4.md) contenant des informations d’imprimante minimales, y compris le nom de l’imprimante, le nom du serveur et si l’imprimante est distante ou locale.<br/> |
| <span id="5"></span><dl> <dt>**5**</dt> </dl> | Une structure [**Printer \_ info \_ 5**](printer-info-5.md) contenant des informations sur l’imprimante, telles que des attributs d’imprimante et des paramètres de délai d’attente.<br/>                                                               |
| <span id="6"></span><dl> <dt>**6**</dt> </dl> | Une structure [**Printer \_ info \_ 6**](printer-info-6.md) spécifiant la valeur d’état d’une imprimante.<br/>                                                                                                      |
| <span id="7"></span><dl> <dt>**7**</dt> </dl> | Une structure d' [**informations d’imprimante \_ \_ 7**](printer-info-7.md) qui indique si l’imprimante est publiée dans le service d’annuaire.<br/>                                                                      |
| <span id="8"></span><dl> <dt>**8**</dt> </dl> | Structure [**d' \_ informations \_ d’imprimante 8**](printer-info-8.md) spécifiant les paramètres d’imprimante par défaut globaux.<br/>                                                                                                |
| <span id="9"></span><dl> <dt>**9**</dt> </dl> | Une structure d' [**informations d’imprimante \_ \_ 9**](printer-info-9.md) spécifiant les paramètres d’imprimante par défaut par utilisateur.<br/>                                                                                              |



 

</dd> <dt>

*cbBuf* \[ dans\]
</dt> <dd>

Taille, en octets, de la mémoire tampon vers laquelle pointe *pPrinter*.

</dd> <dt>

*pcbNeeded* \[ à\]
</dt> <dd>

Pointeur vers une variable dont la fonction définit la taille, en octets, des informations sur l’imprimante. Si la valeur de *cbBuf* est inférieure à cette valeur, **GetPrinter** échoue et la valeur représente la taille de mémoire tampon requise. Si *cbBuf* est supérieur ou égal à cette valeur, **GetPrinter** suit et la valeur représente le nombre d’octets stockés dans la mémoire tampon.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.

Si la fonction échoue, la valeur de retour est égale à zéro.

## <a name="remarks"></a>Notes

> [!Note]  
> Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

Le membre **pDevMode** des structures Printer info [**\_ \_ 2**](printer-info-2.md), [**Printer \_ info \_ 8**](printer-info-8.md)et [**Printer \_ info \_ 9**](printer-info-9.md) peut avoir la **valeur null**. Dans ce cas, l’imprimante est inutilisable jusqu’à ce que le pilote soit réinstallé avec succès.

Pour les structures [**Printer \_ info \_ 2**](printer-info-2.md) et [**Printer \_ info \_ 3**](printer-info-3.md) qui contiennent un pointeur vers un descripteur de sécurité, la fonction récupère uniquement les composants du descripteur de sécurité que l’appelant est autorisé à lire. Pour récupérer des composants de descripteur de sécurité particuliers, vous devez spécifier les droits d’accès nécessaires lorsque vous appelez la fonction [**OpenPrinter**](openprinter.md) pour récupérer un handle vers l’imprimante. Le tableau suivant présente les droits d’accès requis pour lire les différents composants du descripteur de sécurité.



| Droit d'accès                        | Composant descripteur de sécurité                                                                 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| LIRE \_ le contrôle<br/>            | Propriétaire<br/> Groupe principal<br/> Liste de contrôle d’accès discrétionnaire (DACL)<br/> |
| ACCÉDER à la \_ sécurité du système \_<br/> | Liste de contrôle d’accès système (SACL)<br/>                                                  |



 

Si vous spécifiez le niveau 7, le membre **dwAction** de [**Printer \_ info \_ 7**](printer-info-7.md) retourne l’une des valeurs suivantes pour indiquer si l’imprimante est publiée dans le service d’annuaire.



| valeur dwAction     | Signification                                                                                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_publication DSPRINT   | L’imprimante est publiée. Le membre **pszObjectGUID** contient le GUID de l’objet file d’attente à l’impression des services d’annuaire associé à l’imprimante.                                                                                                       |
| DSPRINT \_ annuler la publication | L’imprimante n’est pas publiée.                                                                                                                                                                                                                            |
| DSPRINT \_ en attente   | Indique que le système tente d’effectuer une opération de publication ou d’annulation de publication. Si un appel [**SetPrinter**](setprinter.md) ne parvient pas à publier ou à annuler la publication d’une imprimante, le système effectue d’autres tentatives pour terminer l’opération en arrière-plan. |



 

À compter de Windows Vista, les données d’imprimante retournées par **GetPrinter** sont récupérées à partir d’un cache local lorsque *hPrinter* fait référence à une imprimante hébergée par un serveur d’impression et qu’il y a au moins une connexion ouverte au serveur d’impression. Dans toutes les autres configurations, les données de l’imprimante sont interrogées à partir du serveur d’impression.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Noms Unicode et ANSI<br/>   | **GetPrinterW** (Unicode) et **GetPrinterA** (ANSI)<br/>                                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AbortPrinter**](abortprinter.md)
</dt> <dt>

[**AddPrinter**](addprinter.md)
</dt> <dt>

[**ClosePrinter**](closeprinter.md)
</dt> <dt>

[**DeletePrinter**](deleteprinter.md)
</dt> <dt>

[**EnumPrinters**](enumprinters.md)
</dt> <dt>

[**\_Infos sur l’imprimante \_ 1**](printer-info-1.md)
</dt> <dt>

[**\_Infos sur l’imprimante \_ 2**](printer-info-2.md)
</dt> <dt>

[**\_Infos sur l’imprimante \_ 3**](printer-info-3.md)
</dt> <dt>

[**\_Infos sur l’imprimante \_ 4**](printer-info-4.md)
</dt> <dt>

[**\_Infos sur l’imprimante \_ 5**](printer-info-5.md)
</dt> <dt>

[**\_Infos sur l’imprimante \_ 7**](printer-info-7.md)
</dt> <dt>

[**\_Infos sur l’imprimante \_ 8**](printer-info-8.md)
</dt> <dt>

[**\_Infos sur l’imprimante \_ 9**](printer-info-9.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> </dl>

 

 




