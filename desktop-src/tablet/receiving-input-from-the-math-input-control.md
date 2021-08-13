---
description: Cette section explique comment récupérer le balisage MathML à partir du contrôle d’entrée mathématique à l’aide de l’Active Template Library (ATL) et du modèle COM (Component Object Model).
ms.assetid: 352d2a0c-8275-4fe4-b523-4c74126ffadf
title: Réception d’une entrée du contrôle d’entrée mathématique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50325b8e9980907b91f4cd6400ed6cfd0ef3f04367a2bc753e5d4065e189bc44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449329"
---
# <a name="receiving-input-from-the-math-input-control"></a>Réception d’une entrée du contrôle d’entrée mathématique

Cette section explique comment récupérer le balisage MathML à partir du contrôle d’entrée mathématique à l’aide de l’Active Template Library (ATL) et du modèle COM (Component Object Model).

Pour récupérer l’équation mathématique reconnue à partir du contrôle d’entrée mathématique, vous pouvez remplacer le comportement qui se produit lorsque vous appuyez sur le bouton d’insertion. Pour ce faire, vous devez configurer un gestionnaire d’événements qui implémente les différents événements pris en charge par l’interface [**\_ IMathInputControlEvents**](/windows/win32/api/micaut/nn-micaut-_imathinputcontrolevents) . La configuration du gestionnaire d’événements implique la réalisation des étapes suivantes pour les événements que vous souhaitez prendre en charge (Insert dans ce cas).

-   [Créer une classe de modèle qui contient des récepteurs d’événements](#create-a-template-class-that-contains-event-sinks)
-   [Configurer les gestionnaires d’événements](#set-up-the-event-handlers)
-   [Hériter de la classe de gestionnaire d’événements dans votre classe principale](#inherit-the-event-handler-class-in-your-main-class)
-   [Initialiser votre classe pour hériter du ou des récepteurs d’événements](#initialize-your-class-to-inherit-the-event-sinks)

## <a name="create-a-template-class-that-contains-event-sinks"></a>Créer une classe de modèle qui contient des récepteurs d’événements

Lorsque vous implémentez un récepteur d’événements qui utilise le contrôle d’entrée mathématique, vous devez d’abord spécifier un ID de récepteur. Vous devez ensuite créer une classe de modèle qui hérite de l’événement, du gestionnaire de contrôle d’événements et des interfaces d’événements de contrôle d’entrée mathématique. Le code suivant montre comment définir un ID de récepteur et créer une telle classe de modèle, CMathInputControlEventHandler, qui hérite des interfaces requises. Cette classe de modèle est également configurée pour avoir un pointeur d’interface inconnu privé qui sera utilisé pour passer le contrôle d’entrée mathématique à celle-ci lors de l’initialisation et le \_ membre m ulAdviseCount pour compter le nombre d’appels à Advise/Unadvise.


```
  
#pragma once
static const int MATHINPUTCONTROL_SINK_ID = 1 ;

template <class T>
class ATL_NO_VTABLE CMathInputControlEventHandler :
    public IDispEventSimpleImpl<MATHINPUTCONTROL_SINK_ID, CMathInputControlEventHandler<T>, &__uuidof(_IMathInputControlEvents)>
{
private:
    IUnknown    *m_pUnknown;
    ULONG m_ulAdviseCount;
    CDialog *m_pMain;

```



> [!Note]  
> Le membre **m \_ pMain** doit être différent dans votre implémentation si vous n’utilisez pas de dialogue.

 

Maintenant que vous disposez de la classe de modèle de base, vous devez fournir une déclaration anticipée pour les gestionnaires d’événements que vous allez remplacer et configurer ensuite une table de récepteurs pour les événements que vous allez gérer. Le code suivant montre comment configurer des gestionnaires d’événements pour la méthode [**Insert**](/previous-versions/windows/desktop/legacy/dd317352(v=vs.85)) , appelée lorsqu’un utilisateur clique sur le bouton Insérer dans le contrôle d’entrée mathématique, et la méthode [**Close**](/previous-versions/windows/desktop/legacy/dd317351(v=vs.85)) , appelée lorsqu’un utilisateur clique sur le bouton Annuler dans le contrôle d’entrée mathématique.


```
  
public:
    static const _ATL_FUNC_INFO OnMICInsertInfo; // = {CC_STDCALL, VT_I4, 1, {VT_BSTR}};
    static const _ATL_FUNC_INFO OnMICCloseInfo;  // = {CC_STDCALL, VT_I4, 0, {VT_EMPTY}};

    BEGIN_SINK_MAP(CMathInputControlEventHandler)
        SINK_ENTRY_INFO(MATHINPUTCONTROL_SINK_ID, __uuidof(_IMathInputControlEvents), DISPID_MICInsert, OnMICInsert, const_cast<_ATL_FUNC_INFO*>(&OnMICInsertInfo))
        SINK_ENTRY_INFO(MATHINPUTCONTROL_SINK_ID, __uuidof(_IMathInputControlEvents), DISPID_MICClose, OnMICClose, const_cast<_ATL_FUNC_INFO*>(&OnMICCloseInfo))  
    END_SINK_MAP()
```



Étant donné que vous allez utiliser le contrôle d’entrée mathématique, il est utile de définir une référence interne à l’interface appropriée. La fonction utilitaire suivante est créée dans l’exemple de classe pour définir cette référence.


```
    
  HRESULT Initialize(IUnknown *pUnknown, CDialog *pMain)
  {
    m_pMain  = pMain;
    m_pUnknown = pUnknown;
    m_ulAdviseCount = 0;
    return S_OK;
  }
  
```



## <a name="set-up-the-event-handlers"></a>Configurer les gestionnaires d’événements

Une fois que vous avez configuré les récepteurs d’événements, vous devez créer vos implémentations des récepteurs d’événements. Dans les deux méthodes de l’exemple de code suivant, les récepteurs d’événements récupèrent un descripteur de l’interface de contrôle d’entrée mathématique. Dans la fonction [**Insert**](/previous-versions/windows/desktop/legacy/dd317352(v=vs.85)) , le résultat de la reconnaissance est affiché en tant que MathML et le contrôle est masqué. Dans la fonction [**Close**](/previous-versions/windows/desktop/legacy/dd317351(v=vs.85)) , le contrôle d’entrée mathématique est masqué.


```
  
    // Methods
    HRESULT __stdcall OnMICInsert( BSTR bstrRecoResult)
    {
        CComQIPtr<IMathInputControl> spMIC(m_pUnknown);
        HRESULT hr=S_OK;
        if (spMIC)
        {           
            MessageBox(NULL,bstrRecoResult,L"Recognition Result",MB_OK);
            hr = spMIC->Hide();
            return hr;  
        }
        return E_FAIL;          
    }

    HRESULT __stdcall OnMICClose()
    {
        CComPtr<IMathInputControl> spMIC;
        HRESULT hr = m_pUnknown->QueryInterface<IMathInputControl>(&spMIC);
        if (SUCCEEDED(hr))
        {           
            hr = spMIC->Hide();
            return hr;  
        }
        return hr;                  
    }
};  
```



## <a name="inherit-the-event-handler-class-in-your-main-class"></a>Hériter de la classe de gestionnaire d’événements dans votre classe principale

Une fois que votre classe de modèle est implémentée, vous devez l’hériter de la classe dans laquelle vous allez configurer votre contrôle d’entrée mathématique. Dans le cadre de ce guide, cette classe est une boîte de dialogue, CMIC \_ test \_ EVENTSDlg. Dans l’en-tête de boîte de dialogue, les en-têtes nécessaires doivent être inclus et la classe de modèle que vous avez créée doit être héritée. La classe à laquelle vous héritez et les gestionnaires d’événements doivent avoir des déclarations anticipées afin que le modèle puisse être implémenté. L’exemple de code suivant montre comment procéder.


```
#pragma once
#include <atlbase.h>
#include <atlwin.h>

// include for MIC
#include "micaut.h"

// include for event sinks
#include <iacom.h>
#include "mathinputcontroleventhandler.h"

class CMIC_TEST_EVENTSDlg;

const _ATL_FUNC_INFO CMathInputControlEventHandler<CMIC_TEST_EVENTSDlg>::OnMICInsertInfo = {CC_STDCALL, VT_I4, 1, {VT_BSTR}};
const _ATL_FUNC_INFO CMathInputControlEventHandler<CMIC_TEST_EVENTSDlg>::OnMICCloseInfo = {CC_STDCALL, VT_I4, 0, {VT_EMPTY}};

// CMIC_TEST_EVENTSDlg dialog
class CMIC_TEST_EVENTSDlg : public CDialog,
    public CMathInputControlEventHandler<CMIC_TEST_EVENTSDlg>
{
  public:
  CComPtr<IMathInputControl> m_spMIC; // Math Input Control

  
```



> [!Note]  
> Le type de modèle, **Cmic \_ test \_ EventsDlg**, sera différent, sauf si vous avez nommé votre classe comme dans l’exemple.

 

## <a name="initialize-your-class-to-inherit-the-event-sinks"></a>Initialiser votre classe pour hériter du ou des récepteurs d’événements

Une fois que vous avez configuré votre classe de sorte qu’elle hérite de la classe de modèle, vous êtes prêt à la configurer pour gérer les événements. Cela consiste à initialiser la classe pour avoir un handle vers le contrôle d’entrée mathématique et la classe appelante. En outre, le contrôle d’entrée mathématique pour gérer les événements de doit être envoyé à la méthode DispEventAdvise qui hérite de la classe d’exemple CMathInputControlEventHandler. Le code suivant est appelé à partir de la méthode OnInitDialog dans l’exemple de classe pour effectuer ces actions.


```
// includes for implementation
#include "micaut_i.c"

// include for event handler
#include "mathinputcontroleventhandler.h"

...

OnInitDialog{
  ...

  // TODO: Add extra initialization here
  CoInitialize(NULL);
  HRESULT hr = g_spMIC.CoCreateInstance(CLSID_MathInputControl);
  if (SUCCEEDED(hr)){
    hr = CMathInputControlEventHandler<CMIC_TEST_EVENTSDlg>::Initialize(m_spMIC, this);
      if (SUCCEEDED(hr)){
        hr = CMathInputControlEventHandler<CMIC_TEST_EVENTSDlg>::DispEventAdvise(m_spMIC);            
        if (SUCCEEDED(hr)){
          hr = m_spMIC->Show();  
        }
      }
    }
  }  
}
  
```



> [!Note]  
> Le type de modèle, CMIC \_ test \_ EventsDlg dans cet exemple, sera différent, sauf si vous avez nommé votre classe comme dans l’exemple.

 

 

 
