---
description: Configure l’expert au sein de la DLL de l’expert.
ms.assetid: 3906569d-9ad4-4c03-9637-f4a57697b227
title: Configurer la fonction de rappel (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Configure
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 76ba55b7544e35a07b74a41788a3befa766f87bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106542938"
---
# <a name="configure-callback-function"></a>Configurer la fonction de rappel

La fonction de **configuration** configure l’expert au sein de la dll de l’expert.

L’expert doit implémenter la fonction de **configuration** . Lors de la réception de l’appel de fonction, l’expert affiche une boîte de dialogue qui permet à l’utilisateur de modifier un élément configurable.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI Configure(
  _In_    HEXPERTKEY         hExpertKey,
  _Inout_ PEXPERTCONFIG      *ppConfig,
  _In_    PEXPERTSTARTUPINFO pExpertStartupInfo,
  _In_    DWORD              StartupFlags,
  _In_    HWND               hWnd
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hExpertKey* \[ dans\]
</dt> <dd>

Identificateur d’expert unique.

L’identificateur unique est renvoyé sur toutes les fonctions de Moniteur réseau spécifiques à un expert. N’oubliez pas que l’identificateur peut ne pas être la même clé d’expert que celle transmise à la fonction d' [**exécution**](run.md) . Ne stockez pas la clé d’expert à partir de l’appel de **configuration** .

</dd> <dt>

*ppConfig* \[ in, out\]
</dt> <dd>

Pointeur vers un pointeur vers une structure [**EXPERTCONFIG**](expertconfig.md) à l’entrée.

Après une sortie réussie, la structure [**EXPERTCONFIG**](expertconfig.md) référencée contient les nouvelles données de configuration.

</dd> <dt>

*pExpertStartupInfo* \[ dans\]
</dt> <dd>

Pointeur vers l’élément de capture ayant le focus au démarrage de l’expert.

</dd> <dt>

*StartupFlags* \[ dans\]
</dt> <dd>

Indicateurs qui indiquent comment l’expert doit utiliser le paramètre *pExpertStartupInfo* . Le seul indicateur défini est **l' \_ indicateur de démarrage expert \_ utiliser les données de \_ \_ démarrage \_ sur les \_ \_ \_ données de configuration**. L’indicateur indique que l’expert doit utiliser le paramètre *pExpertStartupInfo* plutôt que le paramètre *ppConfig* qui a été transmis. En règle générale, vous définissez l’indicateur lorsque vous démarrez l’expert à partir d’un menu contextuel.

</dd> <dt>

*HWND* \[ dans\]
</dt> <dd>

Handle de la fenêtre parente. Utilisez la poignée pour ouvrir une boîte de dialogue.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit (autrement dit, s’il existe une configuration en cours), la valeur de retour est **true**.

Si la fonction échoue, la valeur de retour est **false**.

## <a name="remarks"></a>Notes

Moniteur réseau appelle la **fonction de configuration avec** la configuration actuelle de l’expert, le cas échéant. L’expert affiche une boîte de dialogue, dans laquelle vous pouvez modifier n’importe quel élément configurable.

Lorsque *ppConfig* est transmis et que Moniteur réseau n’a pas de configuration stockée pour l’expert spécifié, la valeur du paramètre peut être **null**. Dans ce cas, la fonction **configure** prend en compte les valeurs par défaut codées en dur (ou, utilise les informations de démarrage) pour ouvrir la boîte de dialogue.

Les données de configuration peuvent également être **null** lorsque la fonction **configure** est retournée, et une **valeur null** a été passée. Cette situation se produit lorsque Moniteur réseau n’a pas de valeur par défaut stockée et que l’utilisateur appuie sur **Annuler**.

Le début de la structure de données [**EXPERTCONFIG**](expertconfig.md) comprend une section privée qui stocke les informations de taille de la structure. La taille de la structure **EXPERTCONFIG** doit inclure la longueur **DWORD** réservée qui apparaît au début de la structure. Par exemple, si vos données de configuration nécessitent 20 octets d’espace de stockage, allouez 24 octets pour stocker les données. Si un *ppConfig* a la **valeur null**, la fonction **configure** appelle la fonction [**ExpertAllocMemory**](expertallocmemory.md) pour allouer une nouvelle configuration dont la taille est correcte. Si la mémoire tampon n’est pas suffisante pour contenir les données de l’expert, l’expert doit appeler la fonction [**ExpertReallocMemory**](expertreallocmemory.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




