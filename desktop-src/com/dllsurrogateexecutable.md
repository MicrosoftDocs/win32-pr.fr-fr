---
title: DllSurrogateExecutable
description: Permet aux serveurs DLL de s’exécuter dans un processus de substitution personnalisé, conjointement avec la valeur de Registre DllSurrogate. Si DllSurrogateExecutable n’est pas spécifié, COM transmet NULL comme valeur pour le premier paramètre de la fonction CreateProcess.
ms.assetid: faf5dde3-bd67-447b-a88c-e8660dc5228e
keywords:
- Valeur de Registre DllSurrogateExecutable COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86fc12af22d1f85c2d2e5ff6e75b2904c5fc5eea636a64e314f997ff36a44e38
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119373379"
---
# <a name="dllsurrogateexecutable"></a>DllSurrogateExecutable

Permet aux serveurs DLL de s’exécuter dans un processus de substitution personnalisé, conjointement avec la valeur de Registre [**DllSurrogate**](dllsurrogate.md) . Si **DllSurrogateExecutable** n’est pas spécifié, com transmet **null** comme valeur pour le premier paramètre de la fonction [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) .

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      DllSurrogateExecutable = file
```

## <a name="remarks"></a>Remarques

Cette valeur est de type **reg \_ SZ**. Il fonctionne conjointement avec la valeur [**DllSurrogate**](dllsurrogate.md) pour éviter toute ambiguïté lors de l’utilisation de la fonction [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) . **DllSurrogate** indique si un substitut personnalisé doit être utilisé, et ces informations sont passées en tant que premier paramètre pour **CreateProcess**. Selon l’implémentation de **CreateProcess**, ces informations peuvent être ambiguës. Si **DllSurrogateExecutable** est spécifié, com transmet la valeur en tant que premier paramètre de **CreateProcess**. Si **DllSurrogateExecutable** n’est pas spécifié, com transmet **null** comme valeur pour le premier paramètre de **CreateProcess**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**CoRegisterSurrogate**](/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate)
</dt> <dt>

[Substituts de DLL](dll-surrogates.md)
</dt> <dt>

[**DllSurrogate**](dllsurrogate.md)
</dt> <dt>

[**ISurrogate**](/windows/win32/api/objidlbase/nn-objidlbase-isurrogate)
</dt> </dl>

 

 