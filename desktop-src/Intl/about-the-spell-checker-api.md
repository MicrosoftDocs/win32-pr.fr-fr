---
description: Pour les utilisateurs du monde entier, l’entrée textuelle fait partie d’une expérience informatique moderne, pour les blogs, les commentaires, les tweets, la messagerie instantanée ou tout autre type de texte. dans Windows 8, la vérification orthographique est intégrée pour modifier les contrôles.
ms.assetid: ED569D4F-568B-4381-91C3-8EAEDA4DD47C
title: À propos de l’API vérification orthographique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e3c15594be003b67a6e0c9df62e234e8076cd4ea213bc08468f3bb72698f51f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754939"
---
# <a name="about-the-spell-checking-api"></a>À propos de l’API vérification orthographique

Pour les utilisateurs du monde entier, l’entrée textuelle fait partie d’une expérience informatique moderne, pour les blogs, les commentaires, les tweets, la messagerie instantanée ou tout autre type de texte. dans Windows 8, la vérification orthographique est intégrée pour modifier les contrôles.

Les développeurs peuvent utiliser l’API de vérification orthographique dans leurs applications pour utiliser les services de vérification orthographique disponibles. les développeurs peuvent également créer des vérificateurs d’orthographe qui deviennent des fournisseurs et sont intégrés dans l’infrastructure de vérification orthographique Windows.

l’API vérification orthographique est conçue pour être utilisée par les développeurs professionnels C/C++ de Windows applications COM (component Object Model). l’API de vérification orthographique n’est pas prise en charge pour une utilisation dans un service Windows ou ASP.NET.

## <a name="versioning"></a>Contrôle de version

l’API vérification orthographique est disponible à partir de la Windows 8 ou Windows Server 2012. Les ajouts ultérieurs à l’API seront gérés en créant de nouvelles interfaces qui peuvent être déterminées à l’aide de [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur les interfaces existantes.

## <a name="interfaces"></a>Interfaces

Toutes les interfaces doivent être libérées lorsqu’elles ne sont plus utilisées. Toutes les chaînes **LPWStr** retournées (paramètre de sortie) (et les éléments **LPOLESTR** à partir de [**IEnumString**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring)) doivent être libérées avec [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) quand ils ne sont plus utilisés.

## <a name="error-handling"></a>Gestion des erreurs

Les erreurs sont retournées en tant que **HRESULT** s. [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) et [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) ne sont pas pris en charge dans cette API. Les erreurs ne sont pas particulièrement exploitables, à l’exception des arguments incorrects.

Les codes d’erreur RPC standard peuvent être retournés par l’un des appels d’API, car ils sont hors processus. Les délais d’attente RPC standard s’appliquent.

## <a name="security"></a>Sécurité

L’API vérification orthographique peut charger du code externe (vérificateur orthographique). Il exécute ce code hors processus et dans un contexte de sécurité restreint.

## <a name="dictionary-files"></a>Fichiers de dictionnaire

Les dictionnaires spécifiques à l’utilisateur pour une langue, qui contiennent le contenu pour les listes de mots ajoutées, exclues et à correction automatique, se trouvent sous% AppData% \\ Microsoft \\ orthographe \\ *<language tag>* . Les noms de fichiers sont default. dic (ajouté), default. exclure (excluded) et default. ACL (correction automatique). Les fichiers sont en texte brut UTF-16 qui doit commencer par la marque d’ordre d’octet (BOM) appropriée. Chaque ligne contient un mot (dans les listes de mots ajoutés et exclus) ou une paire de correction automatique avec les mots séparés par une barre verticale (« \| ») (dans la liste de mots correction automatique). Les autres fichiers. dic,. exclure et. ACL présents dans l’annuaire seront détectés par le service de vérification orthographique et ajoutés aux listes de mots utilisateur. Ces fichiers sont considérés comme étant en lecture seule et ne sont pas modifiés par l’API de vérification orthographique.

## <a name="installing-a-spell-checking-provider"></a>Installation d’un fournisseur de vérification orthographique

L’installation d’un fournisseur de vérification orthographique doit placer tous les fichiers qu’il utilise dans un emplacement qui autorise l’accès en lecture à partir du SID ([identificateur de sécurité](../secauthz/security-identifiers.md)) « tous les packages d’application ». Son installation dans un dossier sous « Program Files » fonctionne bien. En outre, le fournisseur doit définir certaines clés dans le registre pour qu’il apparaisse à l’API de vérification orthographique. Il peut se trouver dans la ruche HKEY \_ Current \_ User ou la \_ ruche HKEY local machine, \_ selon qu’elle doit être installée uniquement pour l’utilisateur actuel ou pour tous les utilisateurs.


```
Key: <Registry hive>\SOFTWARE\Classes\CLSID\<Server CLSID>
     Default (REG_SZ) = <Name of the provider>

Key: <Registry hive>\SOFTWARE\Classes\CLSID\<Server CLSID>\InprocServer32
     ThreadingModel (REG_SZ) = "Both"

Key: <Registry hive>\SOFTWARE\Classes\CLSID\<Server CLSID>\Version
     Version (REG_SZ) = <Version>

Key: <Registry hive>\SOFTWARE\Microsoft\Spelling\Spellers\<Provider id string>
     CLSID (REG_SZ) = <CLSID of the COM Server that implements the provider>
```



L' [exemple de fournisseur de vérification orthographique](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerProvider) fournit un exemple de l’inscription nécessaire pour installer un fournisseur.

Si vous créez de nouvelles options de vérification orthographique pour un fournisseur de vérification orthographique, consultez [**IOptionDescription :: ID**](/windows/desktop/api/Spellcheck/nf-spellcheck-ioptiondescription-get_id) pour obtenir de l’aide sur l’affectation de noms.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence de l’API vérification orthographique](spell-checker-api-reference.md)
</dt> <dt>

[Exemple de client de vérification orthographique](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerClient)
</dt> <dt>

[Exemple de fournisseur de vérification orthographique](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerProvider)
</dt> <dt>

[**IOptionDescription :: ID**](/windows/desktop/api/Spellcheck/nf-spellcheck-ioptiondescription-get_id)
</dt> <dt>

[**IEnumString**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring)
</dt> <dt>

[**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))
</dt> </dl>

 

 
