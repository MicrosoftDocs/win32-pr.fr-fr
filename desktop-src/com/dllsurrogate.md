---
title: DllSurrogate
description: Permet aux serveurs DLL de s’exécuter dans un processus de substitution. Si une chaîne vide est spécifiée, le substitut fourni par le système est utilisé ; Sinon, la valeur spécifie le chemin d’accès du substitut à utiliser.
ms.assetid: ae02d828-9cdb-4faa-8fa9-971da97e27b1
keywords:
- Valeur de Registre DllSurrogate COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9854f3c4e4390d64d97c8ab829ac2e7fe34488e6
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382955"
---
# <a name="dllsurrogate"></a>DllSurrogate

Permet aux serveurs DLL de s’exécuter dans un processus de substitution. Si une chaîne vide est spécifiée, le substitut fourni par le système est utilisé ; Sinon, la valeur spécifie le chemin d’accès du substitut à utiliser.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      DllSurrogate = path
```

## <a name="remarks"></a>Notes

Il s’agit d’une valeur de **reg \_ SZ** qui spécifie que la classe est une dll qui doit être activée dans un processus de substitution et le processus de substitution à utiliser. Pour utiliser le processus de substitution générique fourni par le système, définissez le *chemin d’accès* à une chaîne vide ou **null**. Pour spécifier un autre processus de substitution, définissez *path* sur le chemin d’accès du substitut. Comme dans la spécification du chemin d’accès d’un serveur sous la clé [**LocalServer32**](localserver32.md) , une spécification de chemin d’accès complet n’est pas nécessaire. Le substitut doit être écrit pour communiquer correctement avec le service DCOM, comme décrit dans [écriture d’un substitut personnalisé](writing-a-custom-surrogate.md).

La valeur **DllSurrogate** doit être présente pour qu’un serveur dll soit activé dans un substitut. L’activation fait référence à un appel à [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex), **CoCreateInstanceEx**, [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile), [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage)ou [**IMoniker :: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject). L’exécution de dll dans un processus de substitution offre les avantages d’une implémentation exécutable, y compris l’isolation des erreurs, la possibilité de traiter plusieurs clients simultanément et d’autoriser le serveur à fournir des services aux clients distants dans un environnement distribué.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**CoRegisterSurrogate**](/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate)
</dt> <dt>

[Substituts de DLL](dll-surrogates.md)
</dt> <dt>

[**DllSurrogateExecutable**](dllsurrogateexecutable.md)
</dt> <dt>

[**ISurrogate**](/windows/win32/api/objidlbase/nn-objidlbase-isurrogate)
</dt> </dl>

 

 