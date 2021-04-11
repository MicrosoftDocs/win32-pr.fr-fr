---
title: Fonctions de nœud déconseillées
description: Fonctions de nœud déconseillées
ms.assetid: 72833757-a356-4727-8fc8-77a60e26aa99
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7273ffd6c704c9db6408165d1eba3a293f3d1cf
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2020
ms.locfileid: "103941436"
---
# <a name="deprecated-node-functions"></a>Fonctions de nœud déconseillées

> [!Note]  
> Les fonctions de modèle de contrôle décrites dans cette section sont déconseillées. Les applications clientes doivent utiliser les interfaces COM (Component Object Model) décrites dans les sections suivantes :
>
> -   [Interfaces d’élément UI Automation pour les clients](uiauto-entry-uiautoclientinterfaces.md)
> -   [Interface de condition de propriété pour les clients](uiauto-client-propconditioninterfaces.md)
> -   [Interfaces de modèle de contrôle pour les clients](uiauto-client-controlpatterninterfaces.md)
> -   [Interfaces de gestion des événements pour les clients](uiauto-client-eventhandlinginterfaces.md)
> -   [Interfaces de fabrique proxy pour les clients](uiauto-client-proxyfactoryinterfaces.md)

 

## <a name="in-this-section"></a>Dans cette section



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Fonction</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaaddevent"><strong>UiaAddEvent</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Cette fonction est déconseillée. Les applications clientes doivent utiliser les interfaces COM UI Automation de Microsoft à la place.
</blockquote>
<br/> Ajoute un écouteur pour les événements sur un nœud dans l’arborescence UI Automation.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaeventaddwindow"><strong>UiaEventAddWindow</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Cette fonction est déconseillée. Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.
</blockquote>
<br/> Ajoute une fenêtre à l’écouteur d’événements.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nc-uiautomationcoreapi-uiaeventcallback"><em>UiaEventCallback</em></a><br/></td>
<td><blockquote>
[!Note]<br />
Cette fonction est déconseillée. Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.
</blockquote>
<br/> Fonction implémentée par le client qui est appelée par UI Automation lorsqu’un événement est déclenché auquel le client s’est abonné.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaeventremovewindow"><strong>UiaEventRemoveWindow</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Cette fonction est déconseillée. Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.
</blockquote>
<br/> Supprime une fenêtre de l’écouteur d’événements.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiafind"><strong>UiaFind</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Cette fonction est déconseillée. Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.
</blockquote>
<br/> Récupère un ou plusieurs nœuds UI Automation qui correspondent aux critères de recherche.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiageterrordescription"><strong>UiaGetErrorDescription</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Cette fonction est déconseillée. Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.
</blockquote>
<br/> Obtient une chaîne d’erreur pour qu’elle puisse être passée au client. Cette méthode n’est pas utilisée directement par les clients.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetpatternprovider"><strong>UiaGetPatternProvider</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Cette fonction est déconseillée. Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.
</blockquote>
<br/> Récupère un <em>modèle de contrôle</em>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetpropertyvalue"><strong>UiaGetPropertyValue</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Cette fonction est déconseillée. Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.
</blockquote>
<br/> Récupère la valeur d’une propriété UI Automation.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetrootnode"><strong>UiaGetRootNode</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Cette fonction est déconseillée. Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.
</blockquote>
<br/> Récupère le nœud UI Automation racine.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetruntimeid"><strong>UiaGetRuntimeId</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Cette fonction est déconseillée. Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.
</blockquote>
<br/> Récupère l’identificateur d’exécution d’un nœud UI Automation.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetupdatedcache"><strong>UiaGetUpdatedCache</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Cette fonction est déconseillée. Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.
</blockquote>
<br/> Met à jour le cache des valeurs de propriété et des modèles de contrôle.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahpatternobjectfromvariant"><strong>UiaHPatternObjectFromVariant</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Cette fonction est déconseillée. Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.
</blockquote>
<br/> Obtient un objet de modèle de contrôle à partir d’un type <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>Variant</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahtextrangefromvariant"><strong>UiaHTextRangeFromVariant</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Cette fonction est déconseillée. Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.
</blockquote>
<br/> Obtient une plage de texte à partir d’un type <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>Variant</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahuianodefromvariant"><strong>UiaHUiaNodeFromVariant</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Cette fonction est déconseillée. Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.
</blockquote>
<br/> Obtient un HUIANODE à partir d’un type <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>Variant</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uialookupid"><strong>UiaLookupId</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Cette fonction est déconseillée. Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.
</blockquote>
<br/> Obtient l’identificateur entier qui peut être utilisé dans les méthodes qui requièrent un PROPERTYID, PATTERNID, CONTROLTYPEID, TEXTATTRIBUTEID ou EVENTID.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianavigate"><strong>UiaNavigate</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Cette fonction est déconseillée. Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.
</blockquote>
<br/> Navigue dans l’arborescence UI Automation, en extrayant éventuellement les informations mises en cache.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromfocus"><strong>UiaNodeFromFocus</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Cette fonction est déconseillée. Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.
</blockquote>
<br/> Récupère le nœud UI Automation pour l’élément d’interface utilisateur qui a actuellement le focus d’entrée.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromhandle"><strong>UiaNodeFromHandle</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Cette fonction est déconseillée. Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.
</blockquote>
<br/> Récupère le nœud UI Automation associé à une fenêtre.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefrompoint"><strong>UiaNodeFromPoint</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Cette fonction est déconseillée. Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.
</blockquote>
<br/> Récupère le nœud UI Automation pour l’élément au point spécifié.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromprovider"><strong>UiaNodeFromProvider</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Cette fonction est déconseillée. Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.
</blockquote>
<br/> Récupère le nœud UI Automation pour un fournisseur d’éléments bruts.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianoderelease"><strong>UiaNodeRelease</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Cette fonction est déconseillée. Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.
</blockquote>
<br/> Supprime un nœud de la mémoire.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiapatternrelease"><strong>UiaPatternRelease</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Cette fonction est déconseillée. Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.
</blockquote>
<br/> Supprime un objet de modèle alloué de la mémoire.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nc-uiautomationcoreapi-uiaprovidercallback"><em>UiaProviderCallback</em></a><br/></td>
<td><blockquote>
[!Note]<br />
Cette fonction est déconseillée. Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.
</blockquote>
<br/> Fonction définie par l’application qui est appelée par UI Automation pour obtenir un fournisseur côté client pour un élément.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiarectisempty"><strong>UiaRectIsEmpty</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Cette fonction est déconseillée. Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.
</blockquote>
<br/> Obtient une valeur booléenne qui spécifie si les coordonnées de tous les rectangles sont égales à 0.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiarectsetempty"><strong>UiaRectSetEmpty</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Cette fonction est déconseillée. Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.
</blockquote>
<br/> Affecte la valeur 0 aux éléments d’une structure <a href="/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiarect"><strong>UiaRect</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaregisterprovidercallback"><strong>UiaRegisterProviderCallback</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Cette fonction est déconseillée. Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.
</blockquote>
<br/> Inscrit la méthode définie par l’application qui est appelée par UI Automation pour obtenir un fournisseur pour un élément.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaremoveevent"><strong>UiaRemoveEvent</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Cette fonction est déconseillée. Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.
</blockquote>
<br/> Supprime un écouteur pour les événements sur un nœud dans l’arborescence UI Automation.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiasetfocus"><strong>UiaSetFocus</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Cette fonction est déconseillée. Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.
</blockquote>
<br/> Définit le focus d’entrée sur l’élément spécifié dans l’interface utilisateur.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiatextrangerelease"><strong>UiaTextRangeRelease</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Cette fonction est déconseillée. Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.
</blockquote>
<br/> Supprime un objet de la plage de texte allouée de la mémoire.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Clients UI Automation](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

