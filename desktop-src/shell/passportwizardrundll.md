---
description: Lance l’Assistant Passport lorsqu’il est utilisé avec Rundll32.exe.
title: PassportWizardRunDll fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PassportWizardRunDll
api_type:
- DllExport
api_location:
- Netplwiz.dll
ms.assetid: 015c3875-698e-4d80-bbfc-4fc8a71197b7
ms.openlocfilehash: 1678677bcb305b7e5c47d28f5168d1e596ca3e26
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842510"
---
# <a name="passportwizardrundll-function"></a>PassportWizardRunDll fonction)

\[Cette fonction est disponible via Windows XP avec Service Pack 2 (SP2) et Windows Server 2003. Il peut être modifié ou non disponible dans les versions ultérieures de Windows.\]

Lance l’Assistant Passport lorsqu’il est utilisé avec Rundll32.exe.

## <a name="syntax"></a>Syntaxe


```C++
void PassportWizardRunDll(
  _In_ HWND      hwndStub,
  _In_ HINSTANCE hAppInstance,
  _In_ LPTSTR    lpszCmdLine,
  _In_ int       nCmdShow
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hwndStub* \[ dans\]
</dt> <dd>

Type : **HWND**

Handle d’une fenêtre propriétaire. Ce paramètre a généralement la valeur **null**.

</dd> <dt>

*hAppInstance* \[ dans\]
</dt> <dd>

Type : **HINSTANCE**

Handle du fichier bibliothèque, obtenu en tant que valeur de retour de [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)("netplwiz").

</dd> <dt>

*lpszCmdLine* \[ dans\]
</dt> <dd>

Type : **LPTStr**

Données d’argument. Cette valeur sera toujours vide.

</dd> <dt>

*nCmdShow* \[ dans\]
</dt> <dd>

Type : **int**

Définit le mode d’affichage de la fenêtre.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Aucun.

## <a name="remarks"></a>Notes

L’Assistant Passport est utilisé pour obtenir un compte Passport par défaut pour Windows. Un Passport donne à l’utilisateur un accès personnalisé à tous les sites Web MSN et à d’autres sites compatibles Passport à l’aide de l’adresse de messagerie de l’utilisateur. L’utilisation de **PassportWizardRunDll** comme point d’entrée dans le fichier Netplwiz.dll via une commande Rundll32 vous permet de lancer l’Assistant Passport à partir d’une ligne de commande comme s’il s’agissait d’un fichier exécutable.

**PassportWizardRunDll** est utilisé uniquement dans le contexte d’une commande Rundll32.exe comme suit :

**rundll32.exe netplwiz.dll, PassportWizardRunDll**

L’utilisation d’une fonction de point d’entrée avec Rundll32.exe ne ressemble pas à un appel de fonction normal. Le nom de la fonction et le nom du fichier. dll dans lequel elle est stockée sont utilisés uniquement comme paramètres de ligne de commande. La définition de fonction présentée sous la syntaxe est un prototype standard pour toutes les fonctions que vous pouvez appeler à l’aide de rundll32. Les valeurs spécifiques pour *hwndStub*, *hAppInstance* et *nCmdShow* ne sont pas fournies par l’utilisateur, mais sont gérées en arrière-plan par rundll32. **PassportWizardRunDll** n’utilise pas la valeur *lpszCmdLine* , donc aucune donnée supplémentaire n’est requise.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                            |
| En-tête<br/>                   | <dl> <dt>Aucun</dt> </dl>                                 |
| DLL<br/>                      | <dl> <dt>Netplwiz.dll (version 5,60 ou ultérieure)</dt> </dl> |



 

 
