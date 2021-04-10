---
title: Implémentation de l’objet COM d’extension de création d’objet
description: Une extension de création d’objet est un objet COM implémenté en tant que serveur in-proc. Les extensions de création d’objet primaire et secondaire doivent implémenter l’interface IDsAdminNewObjExt.
ms.assetid: 0a8ed0ed-9dcb-4373-b549-7da3f3d9f641
ms.tgt_platform: multiple
keywords:
- Implémentation de l’objet COM d’extension de création d’objet AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05c1a9da94caa300c1277cf6f6030357ca9d573d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104030999"
---
# <a name="implementing-the-object-creation-extension-com-object"></a>Implémentation de l’objet COM d’extension de création d’objet

Une extension de création d’objet est un objet COM implémenté en tant que serveur in-proc. Les extensions de création d’objet primaire et secondaire doivent implémenter l’interface [**IDsAdminNewObjExt**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadminnewobjext) .

## <a name="implementing-idsadminnewobjext"></a>Implémentation de IDsAdminNewObjExt

Lorsque l’Assistant Création d’objet est créé, il initialise chaque extension de création d’objet en appelant la méthode [**IDsAdminNewObjExt :: Initialize**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-initialize) de l’extension. La méthode **Initialize** fournit l’extension avec des informations sur le conteneur dans lequel l’objet est créé, le nom de classe du nouvel objet et des informations sur l’Assistant lui-même. Si l’Assistant Création d’objet démarre pour créer un objet à partir d’un objet existant, le paramètre *pADsCopySource* n’est pas **null**. Dans ce cas, l’extension doit tenter d’obtenir autant de données que possible de l’objet copié.

Une fois l’extension initialisée, la méthode [**IDsAdminNewObjExt :: AddPages**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-addpages) est appelée. L’extension doit ajouter la ou les pages à l’Assistant pendant cette méthode. Une page d’Assistant est créée en remplissant une structure [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) , puis en passant cette structure à la fonction [**CreatePropertySheetPage**](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) . La page est ensuite ajoutée à l’Assistant en appelant la fonction de rappel transmise à **AddPages** dans le paramètre *lpfnAddPage* .

Avant l’affichage de la page d’extension, [**IDsAdminNewObjExt :: setObject**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-setobject) est appelée. Cela fournit l’extension avec un pointeur d’interface [**IADs**](/windows/desktop/api/iads/nn-iads-iads) pour l’objet en cours de création.

Lorsque la page de l’Assistant s’affiche, la page doit gérer et répondre aux messages de notification de l’Assistant nécessaires, tels que [**PSN \_ SetActive**](../controls/psn-setactive.md) et [**PSN \_ WIZNEXT**](../controls/psn-wiznext.md).

Lorsque l’utilisateur remplit toutes les pages de l’Assistant, l’Assistant affiche une page « terminer » qui fournit un résumé des données entrées. L’Assistant obtient ces données en appelant la méthode [**IDsAdminNewObjExt :: GetSummaryInfo**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-getsummaryinfo) pour chacune des extensions. La méthode **GetSummaryInfo** fournit un **BSTR** qui contient les données texte affichées dans la page « Finish ». Une extension de création d’objet n’a pas besoin de fournir des données de synthèse. Dans ce cas, **GetSummaryInfo** doit retourner **E \_ NOTIMPL**. **GetSummaryInfo** est appelé une seule fois pour chaque extension, pas par page. par conséquent, si l’extension de création d’objet ajoute plusieurs pages, l’extension doit combiner les données de synthèse en une seule chaîne.

Quand l’utilisateur clique sur le bouton **Terminer** dans la page « terminer », l’Assistant appelle chacune des méthodes [**IDsAdminNewObjExt :: WriteData**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-writedata) de l’extension avec le contexte de la **\_ \_ \_ prévalidation de DSA NEWOBJ CTX** . Dans ce cas, l’extension doit écrire les données collectées dans les propriétés appropriées à l’aide de la méthode [**IADs ::P ut**](/windows/desktop/api/iads/nf-iads-iads-put) ou [**IADs ::P Utex**](/windows/desktop/api/iads/nf-iads-iads-putex) . L’interface [**IADs**](/windows/desktop/api/iads/nn-iads-iads) est fournie à l’extension dans la méthode [**IDsAdminNewObjExt :: setObject**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-setobject) . L’extension ne doit pas valider les propriétés mises en cache en appelant [**IADs :: setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo). Lorsque toutes les propriétés ont été écrites, l’extension de création d’objet principal valide les modifications en appelant **IADs :: setinfo**. Ce sujet est abordé plus en détail ci-dessous.

Si une erreur se produit, l’extension est avertie de l’erreur et pendant quelle opération elle s’est produite lorsque la méthode [**IDsAdminNewObjExt :: OnError**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-onerror) est appelée.

## <a name="implementing-a-primary-object-creation-wizard"></a>Implémentation d’un assistant de création d’objet principal

L’implémentation d’un assistant de création d’objet principal est identique à un assistant de création d’objet secondaire, à ceci près qu’un assistant de création d’objet principal doit exécuter quelques étapes supplémentaires.

Avant la fermeture de la première page, l’Assistant Création d’objet doit créer l’objet de répertoire temporaire. Pour ce faire, appelez la méthode [**IDsAdminNewObjPrimarySite :: CreateNew**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjprimarysite-createnew) . Un pointeur vers l’interface [**IDsAdminNewObjPrimarySite**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadminnewobjprimarysite) est obtenu en appelant [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) avec **IID \_ IDsAdminNewObjPrimarySite** sur l’interface [**IDsAdminNewObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadminnewobj) qui est passée à [**IDsAdminNewObjExt :: Initialize**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-initialize). La méthode **CreateNew** crée un nouvel objet temporaire et appelle [**IDsAdminNewObjExt :: setObject**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-setobject) pour chaque extension.

Quand un assistant de création d’objet contient plusieurs pages, le système met en œuvre une page « terminer » qui affiche un résumé des informations relatives aux objets à enregistrer. Quand l’utilisateur clique sur le bouton **Terminer** sur la page « terminer », le système appelle chaque méthode [**IDsAdminNewObjExt :: WriteData**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-writedata) de l’extension de création d’objet, puis valide l’objet temporaire dans la mémoire persistante. Toutefois, si l’Assistant Création d’objet ne contient qu’une seule page, les boutons **OK** et **Annuler** s’affichent au lieu des boutons **précédent**, **suivant** et **Annuler** , normalement disponibles dans un Assistant et aucune page « terminer » n’est fournie. Pour cette raison, un Assistant extension de création d’objet à page unique doit appeler [**IDsAdminNewObjPrimarySite :: Commit**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjprimarysite-commit) pour effectuer les opérations d’écriture et d’enregistrement. Une extension de création d’objet principal d’une seule page doit appeler la **validation** en réponse à la notification [**PSN \_ WIZFINISH**](../controls/psn-wizfinish.md) .

Étant donné que d’autres extensions de création d’objets peuvent ajouter des pages à l’Assistant, l’extension de création d’objet principal peut ne pas savoir s’il y a plus d’une page dans l’Assistant. Ce n’est pas un problème pour deux raisons : tout d’abord, si le système implémente la page « terminer », l’extension de la création de l’objet principal recevra la notification [**PSN \_ WIZNEXT**](../controls/psn-wiznext.md) au lieu de la notification **\_ WIZNEXT PSN** . Deuxièmement, la [**validation**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjprimarysite-commit) échouera sans danger si l’Assistant contient plus d’une page.

 

 