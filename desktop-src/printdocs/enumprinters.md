---
description: La fonction EnumPrinters énumère les imprimantes disponibles, les serveurs d’impression, les domaines ou les fournisseurs d’impression.
ms.assetid: 0d0cc726-c515-4146-9273-cdf1db3c76b7
title: EnumPrinters, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinters
- EnumPrintersA
- EnumPrintersW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: fb88cef081010f1319fb194904933ba2366d6593f0d2517c696bb6d6490ace20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119353839"
---
# <a name="enumprinters-function"></a>EnumPrinters fonction)

La fonction **EnumPrinters** énumère les imprimantes disponibles, les serveurs d’impression, les domaines ou les fournisseurs d’impression.

## <a name="syntax"></a>Syntaxe


```C++
BOOL EnumPrinters(
  _In_  DWORD   Flags,
  _In_  LPTSTR  Name,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPrinterEnum,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Indicateurs* \[ dans\]
</dt> <dd>

Types d’objets d’impression que la fonction doit énumérer. Cette valeur peut être une ou plusieurs des valeurs suivantes.



| Valeur                                                                                                                                                                                               | Signification                                                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRINTER_ENUM_LOCAL"></span><span id="printer_enum_local"></span><dl> <dt>**\_enum \_ local de l’imprimante**</dt> </dl>                       | Si l’indicateur de nom d’enum d’imprimante \_ \_ n’est pas également passé, la fonction ignore le paramètre *Name* et énumère les imprimantes installées localement. Si \_ \_ le nom d’enum de l’imprimante est également passé, la fonction énumère les imprimantes locales sur le *nom*. <br/> |
| <span id="PRINTER_ENUM_NAME"></span><span id="printer_enum_name"></span><dl> <dt>**nom de l’enum de l’imprimante \_ \_**</dt> </dl>                          | La fonction énumère l’imprimante identifiée par son *nom*. Il peut s’agir d’un serveur, d’un domaine ou d’un fournisseur d’impression. Si le *nom* est **null**, la fonction énumère les fournisseurs d’impression disponibles.<br/>                                                    |
| <span id="PRINTER_ENUM_SHARED"></span><span id="printer_enum_shared"></span><dl> <dt>**ENUM d’imprimante \_ \_ partagé**</dt> </dl>                    | La fonction énumère les imprimantes qui ont l’attribut Shared. Ne peut pas être utilisé de manière isolée ; Utilisez une opération ou pour combiner avec un autre \_ type d’énumération d’imprimante.<br/>                                                                               |
| <span id="PRINTER_ENUM_CONNECTIONS"></span><span id="printer_enum_connections"></span><dl> <dt>**\_connexions d’énumération d’imprimantes \_**</dt> </dl>     | La fonction énumère la liste des imprimantes auxquelles l’utilisateur a effectué des connexions précédentes.<br/>                                                                                                                                               |
| <span id="PRINTER_ENUM_NETWORK"></span><span id="printer_enum_network"></span><dl> <dt>**\_réseau d’énumération d’imprimantes \_**</dt> </dl>                 | La fonction énumère les imprimantes réseau dans le domaine de l’ordinateur. Cette valeur est valide uniquement si *Level* a la valeur 1.<br/>                                                                                                                                |
| <span id="PRINTER_ENUM_REMOTE"></span><span id="printer_enum_remote"></span><dl> <dt>**IMPRIMANTE \_ \_ à distance enum**</dt> </dl>                    | La fonction énumère les imprimantes réseau et les serveurs d’impression dans le domaine de l’ordinateur. Cette valeur est valide uniquement si *Level* a la valeur 1.<br/>                                                                                                              |
| <span id="PRINTER_ENUM_CATEGORY_3D"></span><span id="printer_enum_category_3d"></span><dl> <dt>**\_Catégorie d’énumération d’imprimantes \_ \_ 3D**</dt> </dl>    | La fonction énumère uniquement les imprimantes 3D.<br/>                                                                                                                                                                                                   |
| <span id="PRINTER_ENUM_CATEGORY_ALL"></span><span id="printer_enum_category_all"></span><dl> <dt>**IMPRIMANTE \_ \_ catégorie \_ tout**</dt> </dl> | La fonction énumère tous les périphériques d’impression, y compris les imprimantes 3D.<br/>                                                                                                                                                                           |



 

Si le *niveau* est 4, vous ne pouvez utiliser que les \_ connexions d’énumération d’imprimante et les \_ \_ \_ constantes d’imprimante locales Enum.

> [!Note]  
> les périphériques d’impression 3D ne sont pas énumérés par défaut. Vous devez inclure à la fois **Printer \_ enum \_ Category \_ 3D** et **Printer \_ enum \_ local** pour énumérer uniquement les imprimantes 3D. Pour inclure des imprimantes 3D, ainsi que toutes les autres imprimantes locales, utilisez l' **\_ énumération d’imprimante \_ catégorie \_ tout** et l' **\_ énumération \_ locale** de l’imprimante.

 

</dd> <dt>

*Nom* \[ dans\]
</dt> <dd>

Si *Level* a la valeur 1, *Flags* contient le nom de l’enum d’imprimante \_ et le \_ *nom* n’est pas **null**, le *nom* est un pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom de l’objet à énumérer. Cette chaîne peut être le nom d’un serveur, d’un domaine ou d’un fournisseur d’impression.

Si *Level* a la valeur 1, *Flags* contient le nom de l’enum d’imprimante \_ \_ et *Name* est **null**, puis la fonction énumère les fournisseurs d’impression disponibles.

Si *Level* a la valeur 1, *Flags* contient Printer \_ enum \_ Remote et *Name* est **null**, alors que la fonction énumère les imprimantes dans le domaine de l’utilisateur.

Si *Level* a la valeur 2 ou 5,*Name* est un pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom d’un serveur dont les imprimantes doivent être énumérées. Si cette chaîne est **null**, la fonction énumère les imprimantes installées sur l’ordinateur local.

Si le *niveau* est 4, le *nom* doit être **null**. La fonction interroge toujours sur l’ordinateur local.

Quand *Name* a la **valeur null**, la définition d' *indicateurs* sur Printer Printer \_ \_ local \| Printer \_ \_ connections énumère les imprimantes installées sur l’ordinateur local. Ces imprimantes incluent celles qui sont physiquement connectées à l’ordinateur local, ainsi que les imprimantes distantes sur lesquelles il dispose d’une connexion réseau.

Si le *nom* n’est pas **null**, la définition des *indicateurs* sur Printer nom enum de l' \_ \_ \| imprimante locale \_ \_ énumère les imprimantes locales qui sont installées sur le *nom* du serveur.

</dd> <dt>

De *niveau* \[ dans\]
</dt> <dd>

Type des structures de données vers lesquelles pointe *pPrinterEnum*. Les valeurs valides sont 1, 2, 4 et 5, qui correspondent aux structures de données [**Printer \_ info \_ 1**](printer-info-1.md), [**Printer \_ info \_ 2**](printer-info-2.md) , [**Printer \_ info \_ 4**](printer-info-4.md)et [**Printer \_ info \_ 5**](printer-info-5.md) .

Cette valeur peut être 1, 2, 4 ou 5.

</dd> <dt>

*pPrinterEnum* \[ à\]
</dt> <dd>

Pointeur vers une mémoire tampon qui reçoit un tableau de structures d' [**informations d’imprimante \_ \_ 1**](printer-info-1.md), d’informations d’imprimante [**\_ \_ 2**](printer-info-2.md), d' [**informations d’imprimante \_ \_ 4**](printer-info-4.md)ou d' [**informations d’imprimante \_ \_ 5**](printer-info-5.md) . Chaque structure contient des données qui décrivent un objet d’impression disponible.

Si le *niveau* est 1, le tableau contient les structures des [**informations d’imprimante \_ \_ 1**](printer-info-1.md) . Si le *niveau* est 2, le tableau contient les structures des [**informations d’imprimante \_ \_ 2**](printer-info-2.md) . Si le *niveau* est 4, le tableau contient les structures de l' [**imprimante \_ info \_ 4**](printer-info-4.md) . Si le *niveau* est 5, le tableau contient les structures des [**informations d’imprimante \_ \_ 5**](printer-info-5.md) .

La mémoire tampon doit être suffisamment grande pour recevoir le tableau de structures de données et toutes les chaînes ou autres données auxquelles les membres de la structure pointent. Si la mémoire tampon est trop petite, le paramètre *pcbNeeded* retourne la taille de mémoire tampon requise.

</dd> <dt>

*cbBuf* \[ dans\]
</dt> <dd>

Taille, en octets, de la mémoire tampon vers laquelle pointe *pPrinterEnum*.

</dd> <dt>

*pcbNeeded* \[ à\]
</dt> <dd>

Pointeur vers une valeur qui reçoit le nombre d’octets copiés si la fonction est réussie ou le nombre d’octets requis si *cbBuf* est trop petit.

</dd> <dt>

*pcReturned* \[ à\]
</dt> <dd>

Pointeur vers une valeur qui reçoit le nombre de structures [**Printer \_ info \_ 1**](printer-info-1.md), [**Printer \_ info \_ 2**](printer-info-2.md) , [**Printer \_ info \_ 4**](printer-info-4.md)ou [**Printer \_ info \_ 5**](printer-info-5.md) que la fonction retourne dans le tableau auquel *pPrinterEnum* pointe.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.

Si la fonction échoue, la valeur de retour est égale à zéro.

## <a name="remarks"></a>Remarques

N’appelez pas cette méthode dans [**DllMain**](/windows/desktop/Dlls/dllmain).

> [!Note]  
> Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

Si **EnumPrinters** retourne une structure d' [**informations d’imprimante \_ \_ 1**](printer-info-1.md) dans laquelle le \_ conteneur d’énumération d’imprimante \_ est spécifié, cela indique qu’il existe une hiérarchie d’objets Printer. Une application peut énumérer la hiérarchie en appelant à nouveau **EnumPrinters** , en affectant à *Name* la valeur du membre **pname** de la structure **\_ info \_ 1** de l’imprimante.

La fonction **EnumPrinters** ne récupère pas les informations de sécurité. Si les structures [**\_ info \_ 2**](printer-info-2.md) de l’imprimante sont retournées dans le tableau pointé par *pPrinterEnum*, leurs membres *pSecurityDescriptor* seront définis sur **null**.

Pour obtenir des informations sur l’imprimante par défaut, appelez [**GetDefaultPrinter**](getdefaultprinter.md).

La structure [**Printer \_ info \_ 4**](printer-info-4.md) offre un moyen simple et extrêmement rapide de récupérer les noms des imprimantes installées sur un ordinateur local, ainsi que les connexions distantes qu’un utilisateur a établies. Quand **EnumPrinters** est appelé avec une structure de données **Printer \_ info \_ 4** , cette fonction interroge le registre pour obtenir les informations spécifiées, puis retourne immédiatement. Cela diffère du comportement de **EnumPrinters** lorsqu’il est appelé avec d’autres niveaux de **structures de données d' \_ informations sur l’imprimante \_ \* *. En particulier, lorsque _* EnumPrinters** est appelé avec une structure de données de niveau 2 ([**Printer \_ info \_ 2**](printer-info-2.md)), il effectue un appel [**OpenPrinter**](openprinter.md) sur chaque connexion à distance. Si une connexion distante est interrompue ou si le serveur distant n’existe plus, ou si l’imprimante distante n’existe plus, la fonction doit attendre que RPC expire et, par conséquent, faire échouer l’appel **OpenPrinter** . Cette opération peut prendre du temps. Le passage d’une structure **Printer \_ info \_ 4** permet à une application de récupérer un minimum d’informations requises ; si des informations plus détaillées sont souhaitées, un appel **EnumPrinters** de niveau 2 suivant peut être effectué.

**Windows Vista :** Les données d’imprimante retournées par **EnumPrinters** sont extraites d’un cache local lorsque la valeur de *Level* est 4.

Le tableau suivant montre la sortie **EnumPrinters** pour les différentes valeurs d' *indicateurs* lorsque le paramètre de *niveau* a la valeur 1.

Dans la colonne paramètre de *nom* de la table, vous devez remplacer un nom approprié pour le fournisseur d’impression, le domaine et l’ordinateur. Par exemple, pour « fournisseur d’impression », vous pouvez utiliser le nom du fournisseur d’impression réseau ou le nom du fournisseur d’impression local. Pour récupérer les noms des fournisseurs d’impression, appelez **EnumPrinters** avec le *nom* défini sur **null**.



| Paramètre *Flags*                                  | Paramètre *Name*                            | Résultat                                                                                            |
|----------------------------------------------------|---------------------------------------------|---------------------------------------------------------------------------------------------------|
| PRINTER \_ \_ local enum local (et non pas le nom enum de l’imprimante \_ \_ ) | Le paramètre *Name* est ignoré.<br/> | Toutes les imprimantes locales.<br/>                                                                    |
| nom de l’enum de l’imprimante \_ \_                                | « Fournisseur d’impression »<br/>                 | Tous les noms de domaine<br/>                                                                       |
| nom de l’enum de l’imprimante \_ \_                                | «Fournisseur d’impression ! Domain<br/>          | Toutes les imprimantes et tous les serveurs d’impression dans le domaine de l’ordinateur<br/>                                |
| nom de l’enum de l’imprimante \_ \_                                | «Fournisseur d’impression !! \\ \\ Usinage<br/>    | Toutes les imprimantes partagées sur l' \\ \\ ordinateur<br/>                                                     |
| nom de l’enum de l’imprimante \_ \_                                | Une chaîne vide, ""<br/>              | Toutes les imprimantes locales.<br/>                                                                    |
| nom de l’enum de l’imprimante \_ \_                                | **NULL**<br/>                         | Tous les fournisseurs d’impression dans le domaine de l’ordinateur<br/>                                           |
| \_connexions d’énumération d’imprimantes \_                         | Le paramètre *Name* est ignoré.<br/> | Toutes les imprimantes distantes connectées<br/>                                                          |
| \_réseau d’énumération d’imprimantes \_                             | Le paramètre *Name* est ignoré.<br/> | Toutes les imprimantes dans le domaine de l’ordinateur<br/>                                                  |
| IMPRIMANTE \_ \_ à distance enum                              | Une chaîne vide, ""<br/>              | Toutes les imprimantes et tous les serveurs d’impression dans le domaine de l’ordinateur<br/>                                |
| IMPRIMANTE \_ \_ à distance enum                              | « Fournisseur d’impression »<br/>                 | Identique au nom de l’enum de l’imprimante \_ \_<br/>                                                            |
| IMPRIMANTE \_ \_ à distance enum                              | «Fournisseur d’impression ! Domain<br/>          | Toutes les imprimantes et tous les serveurs d’impression dans le domaine de l’ordinateur, quel que soit le *domaine* spécifié.<br/> |
| \_Catégorie d’énumération d’imprimantes \_ \_ 3D                        | Le paramètre *Name* est ignoré.<br/> | Seules les imprimantes 3D sont énumérées.<br/>                                                       |
| IMPRIMANTE \_ \_ catégorie \_ tout                       | Le paramètre *Name* est ignoré.<br/> | les imprimantes 3D sont énumérées, ainsi que toutes les autres imprimantes.<br/>                             |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Noms Unicode et ANSI<br/>   | **EnumPrintersW** (Unicode) et **EnumPrintersA** (ANSI)<br/>                                       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinter**](addprinter.md)
</dt> <dt>

[**DeletePrinter**](deleteprinter.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**\_Infos sur l’imprimante \_ 1**](printer-info-1.md)
</dt> <dt>

[**\_Infos sur l’imprimante \_ 2**](printer-info-2.md)
</dt> <dt>

[**\_Infos sur l’imprimante \_ 4**](printer-info-4.md)
</dt> <dt>

[**\_Infos sur l’imprimante \_ 5**](printer-info-5.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> </dl>

 

