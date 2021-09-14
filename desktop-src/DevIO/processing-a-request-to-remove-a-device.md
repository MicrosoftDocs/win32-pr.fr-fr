---
description: Une application reçoit un \_ événement d’appareil DBT DEVICEQUERYREMOVE lorsqu’une fonctionnalité du système a décidé de supprimer un périphérique spécifié.
ms.assetid: 66f6c9f4-93fa-4ee8-adf8-cde4e63f9fb7
title: Traitement d’une demande de suppression d’un appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03f6f1089cae0e4c9db964e3877cac8f8f8d8da4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114293"
---
# <a name="processing-a-request-to-remove-a-device"></a>Traitement d’une demande de suppression d’un appareil

Une application reçoit un événement d’appareil [DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md) lorsqu’une fonctionnalité du système a décidé de supprimer un périphérique spécifié. Lorsque l’application reçoit cet événement, elle doit déterminer si elle utilise l’appareil spécifié et annuler ou préparer la suppression.

Dans l’exemple suivant, une application gère un handle ouvert, hFile, sur le fichier ou l’appareil représenté par FileName. L’application s’inscrit à la notification d’événements d’appareil sur l’appareil sous-jacent en appelant la fonction [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) , à l’aide d’un filtre de notification de type **\_ \_ handle DBT DEVTYP** et en spécifiant la variable hFile dans le membre **\_ handle dbch** du filtre.

L’application traite l’événement d’appareil [DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md) en fermant le descripteur de fichier ouvert sur l’appareil à supprimer. En cas d’annulation de la suppression de ce périphérique, l’application traite l’événement de l’appareil [DBT \_ DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md) pour rouvrir le descripteur de l’appareil. Une fois l’appareil supprimé du système, l’application traite les événements d’appareil [DBT \_ DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md) et [DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md) en annulant l’inscription de son handle de notification pour l’appareil et en fermant les handles qui sont toujours ouverts sur l’appareil.


```C++
#include <windows.h>
#include <dbt.h>
#include <strsafe.h>
  // ...

INT_PTR WINAPI WinProcCallback( HWND hWnd,
                                UINT message,
                                WPARAM wParam,
                                LPARAM lParam )
{
  LPCTSTR FileName = NULL;              // path to the file or device of interest
  HANDLE  hFile = INVALID_HANDLE_VALUE; // handle to the file or device

  PDEV_BROADCAST_HDR    pDBHdr;
  PDEV_BROADCAST_HANDLE pDBHandle;
  TCHAR szMsg[80];

  switch (message)
  {
  //...
  case WM_DEVICECHANGE:
    switch (wParam)
    {
      case DBT_DEVICEQUERYREMOVE:
        pDBHdr = (PDEV_BROADCAST_HDR) lParam;
        switch (pDBHdr->dbch_devicetype)
        {
          case DBT_DEVTYP_HANDLE:
            // A request has been made to remove the device;
            // close any open handles to the file or device

            pDBHandle = (PDEV_BROADCAST_HANDLE) pDBHdr;
            if (hFile != INVALID_HANDLE_VALUE) 
            {
              CloseHandle(hFile);
              hFile = INVALID_HANDLE_VALUE;
            }
        }
        return TRUE;

      case DBT_DEVICEQUERYREMOVEFAILED:
        pDBHdr = (PDEV_BROADCAST_HDR) lParam;
        switch (pDBHdr->dbch_devicetype)
        {
          case DBT_DEVTYP_HANDLE:
            // Removal of the device has failed;
            // reopen a handle to the file or device

            pDBHandle = (PDEV_BROADCAST_HANDLE) pDBHdr;
            hFile = CreateFile(FileName,
                       GENERIC_READ,
                       FILE_SHARE_READ,
                       NULL,
                       OPEN_EXISTING,
                       FILE_ATTRIBUTE_NORMAL,
                       NULL);
            if (hFile == INVALID_HANDLE_VALUE) 
            {
              StringCchPrintf( szMsg, sizeof(szMsg)/sizeof(szMsg[0]), 
                               TEXT("CreateFile failed: %lx.\n"), 
                               GetLastError());
              MessageBox(hWnd, szMsg, TEXT("CreateFile"), MB_OK);
            }
        }
        return TRUE;

      case DBT_DEVICEREMOVEPENDING:
        pDBHdr = (PDEV_BROADCAST_HDR) lParam;
        switch (pDBHdr->dbch_devicetype)
        {
          case DBT_DEVTYP_HANDLE:
          
            // The device is being removed;
            // close any open handles to the file or device

            if (hFile != INVALID_HANDLE_VALUE) 
            {
              CloseHandle(hFile);
              hFile = INVALID_HANDLE_VALUE;
            }

        }
        return TRUE;

      case DBT_DEVICEREMOVECOMPLETE:
        pDBHdr = (PDEV_BROADCAST_HDR) lParam;
        switch (pDBHdr->dbch_devicetype)
        {
          case DBT_DEVTYP_HANDLE:
            pDBHandle = (PDEV_BROADCAST_HANDLE) pDBHdr;
            // The device has been removed from the system;
            // unregister its notification handle

            UnregisterDeviceNotification(
              pDBHandle->dbch_hdevnotify);
              
            // The device has been removed;
            // close any remaining open handles to the file or device

            if (hFile != INVALID_HANDLE_VALUE) 
            {
              CloseHandle(hFile);
              hFile = INVALID_HANDLE_VALUE;
            }

        }
        return TRUE;

      default:
        return TRUE;
    }
  }
  default:
    return TRUE;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types d’événements d’appareil](device-event-types.md)
</dt> </dl>

 

 



