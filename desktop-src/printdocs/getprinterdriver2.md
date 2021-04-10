---
description: La fonction GetPrinterDriver2 récupère les données du pilote pour l’imprimante spécifiée. Si le pilote n’est pas installé sur l’ordinateur local, GetPrinterDriver2 l’installe et affiche l’interface utilisateur dans la fenêtre spécifiée.
ms.assetid: 0d482d28-7668-4734-ba71-5b355c18ddec
title: GetPrinterDriver2, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDriver2
- GetPrinterDriver2W
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: b0a9d2bfe7827a2c0e3db9fff9e8249b73bf5102
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210474"
---
# <a name="getprinterdriver2-function"></a>GetPrinterDriver2 fonction)

La fonction **GetPrinterDriver2** récupère les données du pilote pour l’imprimante spécifiée. Si le pilote n’est pas installé sur l’ordinateur local, **GetPrinterDriver2** l’installe et affiche l’interface utilisateur dans la fenêtre spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
BOOL GetPrinterDriver2(
  _In_opt_ HWND    hWnd,
  _In_     HANDLE  hPrinter,
  _In_opt_ LPTSTR  pEnvironment,
  _In_     DWORD   Level,
  _Out_    LPBYTE  pDriverInfo,
  _In_     DWORD   cbBuf,
  _Out_    LPDWORD pcbNeeded
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HWND* \[ dans, facultatif\]
</dt> <dd>

Handle de la fenêtre qui sera utilisée comme fenêtre parente d’une interface utilisateur, telle qu’une boîte de dialogue, que le pilote affiche au cours de l’installation. Si la valeur de ce paramètre est **null**, l’interface utilisateur du pilote est toujours affichée à l’utilisateur lors de l’installation, mais elle n’a pas de fenêtre parente.

</dd> <dt>

*hPrinter* \[ dans\]
</dt> <dd>

Handle vers l’imprimante pour laquelle les données du pilote doivent être récupérées. Utilisez la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.

</dd> <dt>

*pEnvironment* \[ dans, facultatif\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie l’environnement (par exemple, Windows x86, Windows IA64 ou Windows x64). Si ce paramètre a la **valeur null**, l’environnement actuel de l’application appelante et de l’ordinateur client (pas du serveur d’impression et de l’application de destination) est utilisé.

</dd> <dt>

De *niveau* \[ dans\]
</dt> <dd>

Structure du pilote d’imprimante renvoyée dans la mémoire tampon *pDriverInfo* . Ce paramètre peut prendre les valeurs suivantes.



| Valeur                                                                                                | Signification                                             |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | [**\_Informations sur le pilote \_ 1**](driver-info-1.md)<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | [**\_Informations sur le pilote \_ 2**](driver-info-2.md)<br/> |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | [**\_Informations sur le pilote \_ 3**](driver-info-3.md)<br/> |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | [**\_Informations sur le pilote \_ 4**](driver-info-4.md)<br/> |
| <span id="5"></span><dl> <dt>**5**</dt> </dl> | [**\_Informations sur le pilote \_ 5**](driver-info-5.md)<br/> |
| <span id="6"></span><dl> <dt>**6**</dt> </dl> | [**\_Informations sur le pilote \_ 6**](driver-info-6.md)<br/> |
| <span id="8"></span><dl> <dt>**8**</dt> </dl> | [**\_Informations sur le pilote \_ 8**](driver-info-8.md)<br/> |



 

</dd> <dt>

*pDriverInfo* \[ à\]
</dt> <dd>

Pointeur vers une mémoire tampon qui reçoit une structure contenant des informations sur le pilote, comme spécifié par le *niveau*. La mémoire tampon doit être suffisamment grande pour stocker les chaînes pointées par les membres de la structure.

Pour déterminer la taille de mémoire tampon requise, appelez **GetPrinterDriver2** avec *cbBuf* défini à zéro. **GetPrinterDriver2** échoue, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne une **erreur de \_ \_ mémoire tampon insuffisante** et le paramètre *pcbNeeded* retourne la taille, en octets, de la mémoire tampon nécessaire pour contenir le tableau de structures et leurs données.

</dd> <dt>

*cbBuf* \[ dans\]
</dt> <dd>

Taille, en octets, du tableau auquel *pDriverInfo* pointe.

</dd> <dt>

*pcbNeeded* \[ à\]
</dt> <dd>

Pointeur vers une valeur qui reçoit le nombre d’octets copiés si la fonction est réussie ou le nombre d’octets requis si *cbBuf* est trop petit.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.

Si la fonction échoue, la valeur de retour est égale à zéro. Pour obtenir l’état de retour, appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Notes

Les informations relatives aux pilotes [**\_ \_ 2**](driver-info-2.md), informations sur le pilote [**\_ \_ 3**](driver-info-3.md), informations sur le pilote [**\_ \_ 4**](driver-info-4.md), informations sur le pilote [**\_ \_ 5**](driver-info-5.md), [**\_ informations sur le pilote \_ 6**](driver-info-6.md)et structures [**\_ informations sur le pilote \_ 8**](driver-info-8.md) contiennent le nom du fichier, le chemin d’accès complet et le nom du pilote d’imprimante dans le membre **pDriverPath** . Une application peut utiliser le chemin d’accès et le nom de fichier pour charger un pilote d’imprimante en appelant la fonction [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et en spécifiant le chemin d’accès et le nom de fichier comme argument unique.

La version ANSI de cette fonction, **GetPrinterDriver2A** n’est pas prise en charge et retourne une **erreur \_ non \_ prise en charge**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Noms Unicode et ANSI<br/>   | **GetPrinterDriver2W** (Unicode)<br/>                                                               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinterDriver**](addprinterdriver.md)
</dt> <dt>

[**\_Informations sur le pilote \_ 1**](driver-info-1.md)
</dt> <dt>

[**\_Informations sur le pilote \_ 2**](driver-info-2.md)
</dt> <dt>

[**\_Informations sur le pilote \_ 3**](driver-info-3.md)
</dt> <dt>

[**\_Informations sur le pilote \_ 4**](driver-info-4.md)
</dt> <dt>

[**\_Informations sur le pilote \_ 5**](driver-info-5.md)
</dt> <dt>

[**\_Informations sur le pilote \_ 6**](driver-info-6.md)
</dt> <dt>

[**EnumPrinterDrivers**](enumprinterdrivers.md)
</dt> <dt>

[**GetPrinterDriver**](getprinterdriver.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

