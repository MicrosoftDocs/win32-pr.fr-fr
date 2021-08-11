---
description: La fonction DocumentProperties récupère ou modifie les informations d’initialisation de l’imprimante ou affiche une feuille de propriétés de configuration de l’imprimante pour l’imprimante spécifiée.
ms.assetid: e89a2f6f-2bac-4369-b526-f8e15028698b
title: Fonction DocumentProperties (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DocumentProperties
- DocumentPropertiesA
- DocumentPropertiesW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 349a085cc8f55f391b33dd5048d23a35fdac3c2b33b3771290bcecd9fdbcfc8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118235106"
---
# <a name="documentproperties-function"></a>Fonction DocumentProperties

La fonction **DocumentProperties** récupère ou modifie les informations d’initialisation de l’imprimante ou affiche une feuille de propriétés de configuration de l’imprimante pour l’imprimante spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
LONG DocumentProperties(
  _In_  HWND     hWnd,
  _In_  HANDLE   hPrinter,
  _In_  LPTSTR   pDeviceName,
  _Out_ PDEVMODE pDevModeOutput,
  _In_  PDEVMODE pDevModeInput,
  _In_  DWORD    fMode
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HWND* \[ dans\]
</dt> <dd>

Handle de la fenêtre parente de la feuille de propriétés de configuration de l’imprimante.

</dd> <dt>

*hPrinter* \[ dans\]
</dt> <dd>

Handle d’un objet Printer. Utilisez la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.

</dd> <dt>

*pDeviceName* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom de l’appareil pour lequel la feuille de propriétés de configuration de l’imprimante est affichée.

</dd> <dt>

*pDevModeOutput* \[ à\]
</dt> <dd>

Pointeur vers une structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) qui reçoit les données de configuration d’imprimante spécifiées par l’utilisateur.

</dd> <dt>

*pDevModeInput* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que le système d’exploitation utilise pour initialiser les contrôles de la feuille de propriétés.

Ce paramètre est utilisé uniquement si l’indicateur **DM \_ dans la \_ mémoire tampon** est défini dans le paramètre *fMode* . Si **DM \_ dans la \_ mémoire tampon** n’est pas défini, le système d’exploitation utilise le [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)par défaut de l’imprimante.

</dd> <dt>

*fMode* \[ dans\]
</dt> <dd>

Opérations exécutées par la fonction. Si ce paramètre est égal à zéro, la fonction **DocumentProperties** retourne le nombre d’octets requis par la structure de données [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) du pilote d’imprimante. Sinon, utilisez une ou plusieurs des constantes suivantes pour construire une valeur pour ce paramètre. Notez, toutefois, que pour modifier les paramètres d’impression, une application doit spécifier au moins une valeur d’entrée et une valeur de sortie.



| Valeur                                                                                                                                                          | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DM_IN_BUFFER"></span><span id="dm_in_buffer"></span><dl> <dt>**DM \_ dans la \_ mémoire tampon**</dt> </dl>    | Valeur d’entrée. Avant de demander, de copier ou de mettre à jour, la fonction fusionne les paramètres d’impression actuels du pilote d’imprimante avec les paramètres de la structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) spécifiée par le paramètre *pDevModeInput* . La fonction met à jour la structure uniquement pour les membres spécifiés par le membre **dmFields** de la structure **DEVMODE** . Cette valeur est également définie en tant que **\_ modification DM**. En cas de conflit pendant la fusion, les paramètres de la structure **DEVMODE** spécifiée par *pDevModeInput* remplacent les paramètres d’impression actuels du pilote d’imprimante.<br/> |
| <span id="DM_IN_PROMPT"></span><span id="dm_in_prompt"></span><dl> <dt>**DM \_ dans l' \_ invite**</dt> </dl>    | Valeur d’entrée. La fonction affiche la feuille de propriétés configuration de l’impression du pilote d’imprimante, puis modifie les paramètres de la structure de données [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) de l’imprimante en fonction des valeurs spécifiées par l’utilisateur. Cette valeur est également définie en tant qu' **\_ invite DM**.<br/>                                                                                                                                                                                                                                                                                                         |
| <span id="DM_OUT_BUFFER"></span><span id="dm_out_buffer"></span><dl> <dt>**\_mémoire tampon de sortie DM \_**</dt> </dl> | Valeur de sortie. La fonction écrit les paramètres d’impression actuels du pilote d’imprimante, y compris les données privées, dans la structure de données [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) spécifiée par le paramètre *pDevModeOutput* . L’appelant doit allouer une mémoire tampon suffisamment grande pour contenir les informations. Si les jeux **de \_ \_ mémoires tampons** de bits DM sont clairs, le paramètre *PDevModeOutput* peut avoir la **valeur null**. Cette valeur est également définie en tant que **\_ copie DM**.<br/>                                                                                                                                          |



 

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Si le paramètre *fMode* est égal à zéro, la valeur de retour correspond à la taille de la mémoire tampon requise pour contenir les données d’initialisation du pilote d’imprimante. Notez que cette mémoire tampon peut être plus grande qu’une structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) si le pilote d’imprimante ajoute des données privées à la structure.

Si la fonction affiche la feuille de propriétés, la valeur de retour est **IDOK** ou **IDCANCEL**, selon le bouton sélectionné par l’utilisateur.

Si la fonction n’affiche pas la feuille de propriétés et réussit, la valeur de retour est **IDOK**.

Si la fonction échoue, la valeur de retour est inférieure à zéro.

## <a name="remarks"></a>Notes

> [!Note]  
> Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

La chaîne vers laquelle pointe le paramètre *pDeviceName* peut être obtenue en appelant la fonction [**GetPrinter**](getprinter.md) .

La structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) réellement utilisée par un pilote d’imprimante contient la partie indépendante du périphérique (telle que définie ci-dessus), suivie d’une partie spécifique au pilote qui varie en fonction de la taille et du contenu avec chaque pilote et chaque version du pilote. En raison de la dépendance de ce pilote, il est très important pour les applications d’interroger le pilote sur la taille correcte de la structure **DEVMODE** avant d’allouer une mémoire tampon pour celle-ci.

**Pour apporter des modifications aux paramètres d’impression locaux d’une application, une application doit suivre les étapes suivantes :**

1.  Obtient le nombre d’octets requis pour la structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) complète en appelant **DocumentProperties** et en spécifiant zéro dans le paramètre *fMode* .
2.  Allouez de la mémoire pour la structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) complète.
3.  Obtient les paramètres actuels de l’imprimante en appelant **DocumentProperties**. Transmettez un pointeur vers la structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) allouée à l’étape 2 en tant que paramètre *pDevModeOutput* et spécifiez la valeur du **\_ \_ tampon de sortie DM** .
4.  Modifiez les membres appropriés de la structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) retournée et indiquez les membres qui ont été modifiés en définissant les bits correspondants dans le membre **dmFields** du **DEVMODE**.
5.  Appelez **DocumentProperties** et transmettez à nouveau la structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) modifiée en tant que paramètres *pDevModeInput* et *pDevModeOutput* et spécifiez les valeurs de **\_ \_ mémoire tampon** **DM \_ dans \_ buffer** et DM out (qui sont combinées à l’aide de l’opérateur or). La structure **DEVMODE** retournée par le troisième appel à **DocumentProperties** peut être utilisée comme argument dans un appel à la fonction [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) .

Pour créer un handle vers un contexte de périphérique d’impression à l’aide des paramètres actuels de l’imprimante, il vous suffit d’appeler **DocumentProperties** à deux reprises, comme décrit ci-dessus. Le premier appel obtient la taille du [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) complet et le deuxième appel Initialise le **DEVMODE** avec les paramètres actuels de l’imprimante. Transmettez le **DEVMODE** initialisé à [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) pour obtenir le handle du contexte de périphérique d’impression.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Noms Unicode et ANSI<br/>   | **DocumentPropertiesW** (Unicode) et **DocumentPropertiesA** (ANSI)<br/>                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AdvancedDocumentProperties**](advanceddocumentproperties.md)
</dt> <dt>

[**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca)
</dt> <dt>

[**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

