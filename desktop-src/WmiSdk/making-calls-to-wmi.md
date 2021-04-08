---
description: Les fournisseurs peuvent appeler des méthodes implémentées par WMI à partir de leurs implémentations de méthode.
ms.assetid: 5bfd9d9b-ffe5-4def-a97d-85c4c01223f0
ms.tgt_platform: multiple
title: Appels à WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 534e478336cdd9675e382ef9b089f2d7bc595b03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034557"
---
# <a name="making-calls-to-wmi"></a>Appels à WMI

Les fournisseurs peuvent appeler des méthodes implémentées par WMI à partir de leurs implémentations de méthode. Toutefois, il existe des considérations spéciales lorsqu’un fournisseur appelle l’implémentation WMI d’une méthode [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) à partir de sa propre implémentation de la même méthode. Ces considérations sont importantes, que le fournisseur appelle la version synchrone ou asynchrone de la méthode.

Chaque méthode [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) qu’un fournisseur peut implémenter a un paramètre *pctX* , un pointeur vers une implémentation de l’interface [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) . Lorsque WMI appelle le fournisseur, WMI transmet un pointeur valide dans ce paramètre. Un fournisseur doit toujours passer ce même pointeur dans tous les appels à WMI qu’il effectue lors du traitement des demandes. Le fait de définir *pctX* de manière appropriée peut entraîner le démarrage d’une boucle infinie par WMI.

L’exemple de code suivant montre la méthode correcte pour appeler l’implémentation WMI de [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) à partir d’une implémentation de [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).


```C++
STDMETHODIMP CClassProv::GetObjectAsync (BSTR ObjectPath,
    long lFlags, IWbemContext *pCtx,
    IWbemObjectSink *pHandler)
{
  IWbemClassObject *pclObj = NULL;
  IWbemServices* m_pNamespace;
  HRESULT hr = m_pNamespace->GetObject(
      _bstr_t(L"AClass"), 0, pCtx, &pclObj, 
      NULL );
  pclObj->Release();
  return pHandler->SetStatus(0, hr, NULL, NULL);
}
```



L’exemple de code C++ dans cette rubrique requiert les références suivantes et les \# instructions include pour être compilées correctement.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <comdef.h>
#include <Wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



Les fournisseurs d’instance, de classe et de propriété ne doivent émettre aucun appel à WMI demandant la modification de données pendant la maintenance d’une demande de lecture. Les seuls fournisseurs qui sont des exceptions à cette règle sont des fournisseurs push. Un fournisseur push est un fournisseur de classe qui stocke des données dans l’espace de stockage WMI et s’appuie sur WMI pour gérer les demandes des clients. Lors du traitement d’une demande de lecture, un fournisseur Push peut mettre à jour l’espace de stockage WMI, mais doit définir le paramètre *lFlags* sur la **\_ \_ \_ mise à jour du propriétaire de l’indicateur WBEM** dans l’appel [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) approprié.

Les fournisseurs d’événements ne doivent pas apporter de modifications de classe lors de la maintenance d’un appel. Ils ne peuvent pas non plus émettre des appels liés aux événements, tels que la modification d’un filtre d’événement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Développement d’un fournisseur WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Définition des descripteurs de sécurité espace](setting-namespace-security-descriptors.md)
</dt> <dt>

[Sécurisation de votre fournisseur](securing-your-provider.md)
</dt> </dl>

 

 



