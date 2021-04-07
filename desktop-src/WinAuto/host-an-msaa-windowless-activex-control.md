---
title: Comment héberger un contrôle ActiveX sans fenêtre MSAA
description: Découvrez comment créer un conteneur de contrôle qui peut héberger des contrôles Microsoft ActiveX sans fenêtre qui implémentent Microsoft Active Accessibility.
ms.assetid: 9497561C-37ED-4094-A6B0-C219F63C04B6
keywords:
- MSAA, contrôle ActiveX sans fenêtre
- Contrôle ActiveX sans fenêtre, MSAA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9de45313b19490af3c3fffb633f3822ad93d25a4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727524"
---
# <a name="how-to-host-an-msaa-windowless-activex-control"></a>Comment héberger un contrôle ActiveX sans fenêtre MSAA

Découvrez comment créer un conteneur de contrôle qui peut héberger des contrôles Microsoft ActiveX sans fenêtre qui implémentent Microsoft Active Accessibility. En suivant les étapes décrites ici, vous pouvez vous assurer que tous les contrôles sans fenêtre basés sur Microsoft Active Accessibility hébergés dans votre conteneur de contrôle sont accessibles aux applications clientes de la technologie d’assistance (AT).

## <a name="what-you-need-to-know"></a>Ce que vous devez savoir

### <a name="technologies"></a>Technologies

-   [Contrôles ActiveX](/windows/desktop/com/activex-controls)
-   [Microsoft Active Accessibility](microsoft-active-accessibility.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Programmation Microsoft Win32 et COM (Component Object Model)
-   Contrôles ActiveX sans fenêtre
-   Serveurs Microsoft Active Accessibility

## <a name="instructions"></a>Instructions

### <a name="step-1-provide-the-root-iaccessible-interface-on-behalf-of-the-windowless-control"></a>Étape 1 : fournissez l’interface IAccessible racine pour le compte du contrôle sans fenêtre.

Chaque fois que le système a besoin du pointeur [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pour la racine d’un contrôle sans fenêtre, le système interroge le conteneur de contrôle. Pour récupérer le pointeur, le conteneur appelle l’implémentation du contrôle sans fenêtre de la méthode [**IServiceProvider :: QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) .

Si le conteneur de contrôle a une implémentation Microsoft Active Accessibility, il peut retourner le pointeur [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) du contrôle sans fenêtre au système.

Si le conteneur de contrôle a une implémentation de Microsoft UI Automation, appelez la fonction [**UiaProviderFromIAccessible**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaproviderfromiaccessible) pour obtenir un pointeur d’interface [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) qui représente le contrôle, puis retournez le pointeur d’interface **IRawElementProviderSimple** au système.

### <a name="step-2-respond-to-the-wm_getobject-message-on-behalf-of-the-windowless-control"></a>Étape 2 : répondre au message WM \_ GETOBJECT pour le compte du contrôle sans fenêtre.

Lorsqu’une application cliente répond à un WinEvent déclenché par un contrôle sans fenêtre, le conteneur de contrôle reçoit un message [**WM \_ GETOBJECT**](wm-getobject.md) pour le compte du contrôle. Le message contient l’ID d’objet du contrôle sans fenêtre qui a déclenché l’événement.

Le conteneur de contrôle répond en recherchant le contrôle sans fenêtre qui « possède » l’ID de l’objet, puis en appelant la méthode [**IAccessibleHandler :: AccessibleObjectFromID**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessiblehandler-accessibleobjectfromid) de ce contrôle. La méthode **AccessibleObjectFromID** retourne le pointeur d’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pour l’élément d’interface utilisateur, et le conteneur de contrôle retourne le pointeur vers le système, qui le transfère à l’application cliente.

### <a name="step-3-implement-the-iaccessiblewindowlesssite-interface"></a>Étape 3 : implémenter l’interface IAccessibleWindowlessSite.

1.  Implémentez la méthode [**IAccessibleWindowlessSite :: GetParentAccessible**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-getparentaccessible) .

    Lorsqu’une application cliente a besoin d’informations d’accessibilité sur le parent du fournisseur racine du contrôle sans fenêtre, le système appelle la méthode [**IAccessible :: obtenir \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) du contrôle sans fenêtre. Le contrôle répond en appelant la méthode [**IAccessibleWindowlessSite :: GetParentAccessible**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-getparentaccessible) du conteneur de contrôle, qui fournit le pointeur [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) du parent du contrôle sans fenêtre.

2.  Implémentez les méthodes [**IAccessibleWindowlessSite :: AcquireObjectIdRange**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-acquireobjectidrange), [**QueryObjectIdRange**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-queryobjectidranges)et [**ReleaseObjectIdRange**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-releaseobjectidrange) .

    Votre conteneur de contrôle doit conserver un mappage des plages d’ID d’objet aux contrôles sans fenêtre. Le mappage permet au conteneur de contrôle d’identifier le contrôle qui doit répondre à une demande particulière pour un ID d’objet. Le tableau suivant montre un exemple de mappage d’ID d’objet à des contrôles sans fenêtre.

    

    | Base de plage | Taille de la plage | Contrôler   |
    |------------|------------|-----------|
    | 1 000       | 500        | Contrôle 1 |
    | 1500       | 1 000       | Contrôle 2 |
    | 2 500       | 2000       | Contrôle 1 |

    

     

    Le conteneur de contrôle doit conserver le mappage entre les plages d’ID d’objet et les contrôles sans fenêtre pour lui-même et tous les enfants sans fenêtre. Les plages d’ID de l’objet n’ont pas besoin d’être adjacentes les unes aux autres. En outre, pour éviter les attaques par déni de service, le conteneur de contrôle peut placer des limites sur le nombre de plages accordées à un contrôle particulier. Toutefois, il est utile d’autoriser plus d’une plage par contrôle pour permettre à un contrôle de croître.

### <a name="step-4-optional-implement-the-iaccessiblehostingelementproviders-interface"></a>Étape 4 : facultatif : implémentez l’interface IAccessibleHostingElementProviders.

Implémentez l’interface [**IAccessibleHostingElementProviders**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessiblehostingelementproviders) si votre conteneur de contrôle a une implémentation de Microsoft Active Accessibility Server et que le serveur est la racine d’une arborescence d’accessibilité qui inclut des contrôles ActiveX sans fenêtre qui prennent en charge l’Automation d’interface utilisateur. L’interface **IAccessibleHostingElementProviders** possède une méthode unique, [**GetEmbeddedFragmentRoots**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-getembeddedfragmentroots), qui récupère les pointeurs d’interface [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot) de tous les contrôles ActiveX UI Automation qui sont hébergés par votre conteneur de contrôle.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Comment héberger un contrôle ActiveX UI Automation sans fenêtre](host-a-ui-automation-windowless-activex-control.md)
</dt> <dt>

[Accessibilité des contrôles ActiveX sans fenêtre](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 