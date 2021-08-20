---
description: Les extensions de composant logiciel enfichable d’attachement doivent implémenter l’interface ISceSvcAttachmentPersistInfo.
ms.assetid: fadd2e06-d27c-4938-ad0e-ae7beab25931
title: Implémentation de ISceSvcAttachmentPersistInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edaf4f31007225e95914f42d27297347799f53fe3ca2735cac38c6c0d881cebf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117969326"
---
# <a name="implementing-iscesvcattachmentpersistinfo"></a>Implémentation de ISceSvcAttachmentPersistInfo

Les extensions de composant logiciel enfichable d’attachement doivent implémenter l’interface [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) . Les composants logiciels enfichables de configuration de la sécurité interrogent cette interface régulièrement, par exemple lors de l’enregistrement de la configuration ou de la fermeture du composant logiciel enfichable. Cela permet à l’extension de composant logiciel enfichable d’enregistrer toutes les modifications apportées par l’utilisateur à la base de données d’inspection ou à la configuration associée.

L’exemple suivant montre une façon d’implémenter [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo).


```C++
#include <windows.h>

class CSceSvcAttachmentPersistInfo:
  public ISceSvcAttachmentPersistInfo,
  public CComObjectRoot
{
    BEGIN_COM_MAP(CSceSvcAttachmentPersistInfo)
    COM_INTERFACE_ENTRY(ISceSvcAttachmentPersistInfo)
    END_COM_MAP()

    friend class CDataObject;
    friend class CComponentDataImpl;

    CSceSvcAttachmentPersistInfo();
    ~CSceSvcAttachmentPersistInfo();

public:

    // ISceSvcAttachmentPersistInfo interface members
    STDMETHOD(IsDirty)(LPTSTR lpTemplateName);
    STDMETHOD(Save)(LPTSTR lpTemplateName, SCESVC_HANDLE *pscesvcHandle,
         PVOID *ppvData, PBOOL pbOverwriteAll );
    STDMETHOD(FreeBuffer)(PVOID pvData);

    //...

};

//
// Implementing IsDirty
//
STDMETHODIMP CSceSvcAttachmentPersistInfo::IsDirty(LPTSTR lpTemplateName)
{
  if ( m_pSnapin == NULL ) 
  {
    return S_FALSE;
  }
  //
  // just calling the snap-in's main IsDirty
  //
  return m_pSnapin->IsDirty();
}

//
// Implementing Save
//
STDMETHODIMP CSceSvcAttachmentPersistInfo::Save(LPTSTR lpTemplateName,
       SCE_HANDLE *psceHandle, 
       PVOID *ppvData, 
       PBOOL pbOverwriteAll )
{
  if ( psceHandle == NULL || ppvData == NULL || 
       pbOverwriteAll == NULL ) 
  {
    return E_INVALIDARG;
  }

  if ( m_pSnapin != NULL ) 
  {

    m_pSnapin->SaveDataInBuffer(lpTemplateName, psceHandle,
       ppvData, pbOverwriteAll);

    *psceHandle = m_sceHandle;

  }

  return S_OK;
}

//
// Implementing FreeBuffer
//
STDMETHODIMP CSceSvcAttachmentPersistInfo::FreeBuffer(PVOID pvData)
{
  if ( pvData == NULL ) 
  {
    return S_OK;
  }

  PSCESVC_ANALYSIS_INFO pTempInfo=(PSCESVC_ANALYSIS_INFO)pvData;

  if ( pTempInfo->Lines != NULL ) 
  {

    for ( DWORD i=0; i < pTempInfo->Count; i++ ) 
    {

      if ( pTempInfo->Lines[i].Key != NULL )
        LocalFree(pTempInfo->Lines[i].Key);

      if ( pTempInfo->Lines[i].Value != NULL )
        LocalFree(pTempInfo->Lines[i].Value);
    }

    LocalFree( pTempInfo->Lines);
  }

  LocalFree(pTempInfo);

  return S_OK;
}
```



 

 



