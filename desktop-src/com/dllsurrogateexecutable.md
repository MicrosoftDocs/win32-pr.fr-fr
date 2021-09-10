---
title: DllSurrogateExecutable
description: Permet aux serveurs DLL de s’exécuter dans un processus de substitution personnalisé, conjointement avec la valeur de Registre DllSurrogate. Si DllSurrogateExecutable n’est pas spécifié, COM transmet NULL comme valeur pour le premier paramètre de la fonction CreateProcess.
ms.assetid: faf5dde3-bd67-447b-a88c-e8660dc5228e
keywords:
- Valeur de Registre DllSurrogateExecutable COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877297673b0a518006ecf903f447984f9023da34
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363567"
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

 

 