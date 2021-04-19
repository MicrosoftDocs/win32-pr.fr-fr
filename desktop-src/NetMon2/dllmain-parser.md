---
description: La fonction d’exportation DllMain de l’analyseur identifie l’existence de l’analyseur et libère les ressources que Moniteur réseau utilise pour l’analyseur. DllMain doit être implémenté dans toutes les dll de l’analyseur.
ms.assetid: 2ce79d49-3aad-461f-99cf-cf632680efcc
title: Fonction de rappel de l’analyseur DllMain (Process. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DllMain
api_type:
- UserDefined
api_location:
- process.h
ms.openlocfilehash: 1db69d51f3a46bbe219ef7f7bdea67e8e8970e4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538906"
---
# <a name="dllmain-parser-callback-function"></a>Fonction de rappel de l’analyseur DllMain

La fonction d’exportation **DllMain** de l’analyseur identifie l’existence de l’analyseur et libère les ressources que Moniteur réseau utilise pour l’analyseur. **DllMain** doit être implémenté dans toutes les dll de l’analyseur.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI DllMain(
  _In_ HANDLE hInstance,
  _In_ ULONG  Command,
       LPVOID Reserved
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HINSTANCE* \[ dans\]
</dt> <dd>

Handle vers une instance de l’analyseur.

</dd> <dt>

*Commande* \[ dans\]
</dt> <dd>

Indicateur pour déterminer la raison pour laquelle la fonction est appelée. Pour obtenir la liste de tous les indicateurs possibles, consultez [DllMain](/windows/desktop/Dlls/dllmain). L’implémentation de l’analyseur doit traiter les valeurs suivantes.



| Valeur                                                                                                                                                                         | Signification                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DLL_PROCESS_ATTACH"></span><span id="dll_process_attach"></span><dl> <dt>**\_attachement du processus dll \_**</dt> </dl> | Quand **DllMain** est appelée pour la première fois, la dll doit appeler [CreateProtocol](createprotocol.md) pour fournir des informations à Moniteur réseau. <br/>   |
| <span id="DLL_PROCESS_DETACH"></span><span id="dll_process_detach"></span><dl> <dt>**\_détachement de processus dll \_**</dt> </dl> | Quand **DllMain** est appelée pour la dernière fois, la dll doit appeler [DestroyProtocol](destroyprotocol.md) pour libérer les ressources utilisées par la dll. <br/> |



 

</dd> <dt>

*Reserved* 
</dt> <dd>

Non utilisé maintenant.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La DLL de l’analyseur retourne toujours la **valeur true**.

## <a name="remarks"></a>Notes

Le système d’exploitation appelle **DllMain** pour charger et décharger la dll de l’analyseur. Cette fonction est basée sur la fonction [DllMain](/windows/desktop/Dlls/dllmain) de la bibliothèque de liens dynamiques.

Vous pouvez également utiliser l’implémentation de **DllMain** pour stocker une instance d’un analyseur pour une utilisation ultérieure. Par exemple, vous pouvez stocker une instance de DLL de l’analyseur, puis l’utiliser pour un appel système à l’avenir.



| Pour plus d’informations sur                                        | Consultez                                                     |
|-----------------------------------------------------------|---------------------------------------------------------|
| Ce que sont les analyseurs et comment ils fonctionnent avec Moniteur réseau. | [Analyseurs](parsers.md)                                  |
| Les points d’entrée inclus dans la DLL de l’analyseur.        | [Architecture des DLL de l’analyseur](parser-dll-architecture.md)  |
| L’implémentation de **DllMain**  comprend un exemple.        | [Implémentation de DllMain](implementing-dllmain-parser.md) |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Process. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[CreateProtocol](createprotocol.md)
</dt> <dt>

[DestroyProtocol](destroyprotocol.md)
</dt> <dt>

[DllMain](/windows/desktop/Dlls/dllmain)
</dt> </dl>

 

