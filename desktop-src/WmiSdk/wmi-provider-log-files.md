---
description: Les fournisseurs WMI peuvent également conserver les journaux. Les fichiers journaux qui apparaissent sur un système dépendent des fournisseurs installés.
ms.assetid: 04f041e5-4f2c-4c94-9aba-b040d941b46d
ms.tgt_platform: multiple
title: Fichiers journaux du fournisseur WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed9cc74b9f1c6be16f1d85eb1e1863e0dc8b7b33
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880003"
---
# <a name="wmi-provider-log-files"></a>Fichiers journaux du fournisseur WMI

Les fournisseurs WMI peuvent également conserver les journaux. Les fichiers journaux qui apparaissent sur un système dépendent des fournisseurs installés.

Ces journaux peuvent se trouver dans le répertoire% SystemRoot% \\ system32 \\ WBEM \\ logs.

-   [Wmiprov. log](#wmiprovlog)
-   [Ntevt. log](#ntevtlog)
-   [Dsprovider. log](#dsproviderlog)
-   [Rubriques connexes](#related-topics)

## <a name="wmiprovlog"></a>Wmiprov. log

le fichier Wmiprov. log contient les données de gestion et les événements des pilotes Windows Driver Model wdm (compatible WMI) et du [fournisseur wdm](/windows/desktop/WmiCoreProv/wdm-provider). Il fournit des informations d’avertissement et d’erreur principalement pour le dépannage et le débogage des applications fournisseur et client qui l’utilisent.

Wmiprov. log contient les éléments suivants :

-   Les erreurs du [fournisseur WDM](/windows/desktop/WmiCoreProv/wdm-provider) ou du pilote de périphérique, telles que la compilation binaire MOF, échouent ou ne parviennent pas à récupérer des données.
-   État de la compilation MOF pour chacun des pilotes qui utilisent le format MOF.
-   Événements de construction et de déconstruction du fournisseur.
-   Impression de WNODE.

## <a name="ntevtlog"></a>Ntevt. log

Le fichier ntevt. log contient des messages de suivi du [fournisseur du journal des événements](/previous-versions/windows/desktop/eventlogprov/event-log-provider).

## <a name="dsproviderlog"></a>Dsprovider. log

Le fichier Dsprovider. log contient des informations de suivi et des messages d’erreur pour le [fournisseur Active Directory](/previous-versions/windows/desktop/dsprov/active-directory-provider).

Le tableau suivant répertorie certains problèmes courants qui peuvent se produire et fournit des causes et des solutions possibles.



| Message                                                                                                                                                                                                                                                                                                        | Description                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ÉCHEC de CLDAPClassProvider :: InitializeLDAPProvider ADsGetObject sur RootDSE : &lt; HRESULT&gt;                                                                                                                                                                                                                    | L’appel ADSI a échoué lors de la tentative d’extraction de la racine de vos services d’annuaire. Vérifiez que votre ordinateur est membre d’un domaine.                                                                                                                                                                                                                                                                             |
| ÉCHEC de CDSClassProvider :: GetObjectAsync () GetClassFromCacheOrADSI <class name> avec &lt; HRESULT&gt;                                                                                                                                                                                                  | La classe que vous essayez d’obtenir n’est pas une classe valide dans le répertoire. Vérifiez que le nom de la classe est correct.                                                                                                                                                                                                                                                                                                |
| CLDAPInstanceProvider ::P utInstanceAsync () ModifyExistingInstance a échoué pour LDAP : 0408 = foo1, CN = Users, DC = dsprovider, DC = nttest, DC = Microsoft, DC = com avec &lt; HRESULT&gt;                                                                                                                                       | Le fournisseur n’a pas pu écrire une instance modifiée dans les services d’annuaire. Vérifiez que vous utilisez l’interface [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) pour spécifier l’ensemble de propriétés que vous modifiez. Pour plus d’informations sur l’utilisation de l’interface **IWbemContext** avec [**PutInstance**](/windows/desktop/api/Provider/nf-provider-provider-putinstance(constcinstance__long)), consultez [mise à jour d’une instance entière](updating-an-entire-instance.md). |
| CLDAPHelper :: GetADSIInstance ADsOpenObject () a échoué sur <class name> avec &lt; HRESULT&gt;<br/> CLDAPInstanceProvider :: GetObjectAsync : échec de GetADSIInstance () avec &lt; HRESULT&gt;<br/> CLDAPInstanceProvider :: GetObjectAsync () a échoué pour l' \_ utilisateur DS. ADSIPath = "<class name><br/> | Ces trois messages indiquent que l’instance que vous essayez d’extraire n’existe pas dans le service d’annuaire. Vérifiez que la valeur **ADSIPath** et le nom de la classe sont corrects.                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fichiers journaux WMI](wmi-log-files.md)
</dt> </dl>

 

