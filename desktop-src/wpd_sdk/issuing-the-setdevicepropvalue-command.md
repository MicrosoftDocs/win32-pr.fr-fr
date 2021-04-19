---
description: Émission de la commande SetDevicePropValue
ms.assetid: d5917421-fbd4-477c-b29b-9f983c93cfdb
title: Émission de la commande SetDevicePropValue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8949cbf4fe22662de32c4c07de689fec2e6dbad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534141"
---
# <a name="issuing-the-setdevicepropvalue-command"></a><span data-ttu-id="0950d-103">Émission de la commande SetDevicePropValue</span><span class="sxs-lookup"><span data-stu-id="0950d-103">Issuing the SetDevicePropValue Command</span></span>

<span data-ttu-id="0950d-104">L’exemple de cette section appelle la commande MTP **SetDevicePropValue** .</span><span class="sxs-lookup"><span data-stu-id="0950d-104">The example in this section invokes the **SetDevicePropValue** MTP command.</span></span> <span data-ttu-id="0950d-105">(Pour obtenir une description complète de cette commande et de ses paramètres, consultez la [spécification MTP](https://www.usb.org/sites/default/files/MTPv1_1.zip).)</span><span class="sxs-lookup"><span data-stu-id="0950d-105">(For a complete description of this command and its parameters, see the [MTP specification](https://www.usb.org/sites/default/files/MTPv1_1.zip).)</span></span>

<span data-ttu-id="0950d-106">Comme cette commande comprend des données (ou une phase de données), elle est plus complexe que l' [exemple](issuing-the-getnumobjects-command.md)précédent.</span><span class="sxs-lookup"><span data-stu-id="0950d-106">Because this command includes data (or a data phase), it is more involved than the previous [example](issuing-the-getnumobjects-command.md).</span></span> <span data-ttu-id="0950d-107">Les commandes qui incluent une phase de données peuvent être divisées en trois parties :</span><span class="sxs-lookup"><span data-stu-id="0950d-107">Commands that include a data phase can be broken into three parts:</span></span>

1.  <span data-ttu-id="0950d-108">Initiation : l’application initie la commande en informant l’appareil que les données sont arrivées ou attendues.</span><span class="sxs-lookup"><span data-stu-id="0950d-108">Initiation: The application initiates the command by informing the device that data is either coming or expected.</span></span>
2.  <span data-ttu-id="0950d-109">Transfert : l’application transfère les données (en écrivant ou en lisant les données).</span><span class="sxs-lookup"><span data-stu-id="0950d-109">Transfer: The application transfers the data (either by writing or reading the data).</span></span>
3.  <span data-ttu-id="0950d-110">Achèvement : l’application (ou l’appareil) signale que la commande est terminée et récupère un code de réponse.</span><span class="sxs-lookup"><span data-stu-id="0950d-110">Completion: The application (or the device) signals that the command is complete and retrieves a response code.</span></span>

<span data-ttu-id="0950d-111">La liste précédente se traduit par la séquence de commandes suivante :</span><span class="sxs-lookup"><span data-stu-id="0950d-111">The previous list translates into the following command sequence:</span></span>

1.  <span data-ttu-id="0950d-112">Commande \_ wpd \_ MTP \_ ext \_ Execute \_ Command \_ , avec les données \_ \_ à \_ écrire ou la commande wpd \_ \_ MTP \_ ext \_ Execute \_ Command \_ , avec les \_ données \_ à \_ lire.</span><span class="sxs-lookup"><span data-stu-id="0950d-112">WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_WRITE or WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_READ.</span></span>
2.  <span data-ttu-id="0950d-113">\_Commande wpd \_ MTP \_ ext \_ Write \_ Data ou la \_ commande wpd \_ MTP \_ ext \_ Read \_ Data.</span><span class="sxs-lookup"><span data-stu-id="0950d-113">WPD\_COMMAND\_MTP\_EXT\_WRITE\_DATA or WPD\_COMMAND\_MTP\_EXT\_READ\_DATA.</span></span>
3.  <span data-ttu-id="0950d-114">\_transfert de \_ données de fin MTP MTP de la commande wpd \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="0950d-114">WPD\_COMMAND\_MTP\_EXT\_END\_DATA\_TRANSFER.</span></span>

<span data-ttu-id="0950d-115">Dans le cas de **SetDevicePropValue**, l’exemple de code utilise la séquence suivante :</span><span class="sxs-lookup"><span data-stu-id="0950d-115">In the case of **SetDevicePropValue**, the sample code uses the following sequence:</span></span>

1.  <span data-ttu-id="0950d-116">commande \_ wpd \_ MTP \_ ext \_ Execute \_ Command \_ avec les \_ données \_ à \_ écrire.</span><span class="sxs-lookup"><span data-stu-id="0950d-116">WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_WRITE.</span></span>
2.  <span data-ttu-id="0950d-117">\_données d' \_ écriture MTP ext de la commande wpd \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="0950d-117">WPD\_COMMAND\_MTP\_EXT\_WRITE\_DATA.</span></span>
3.  <span data-ttu-id="0950d-118">\_transfert de \_ données de fin MTP MTP de la commande wpd \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="0950d-118">WPD\_COMMAND\_MTP\_EXT\_END\_DATA\_TRANSFER.</span></span>

<span data-ttu-id="0950d-119">L’exemple de code suivant montre comment une application WPD lance la séquence de commandes.</span><span class="sxs-lookup"><span data-stu-id="0950d-119">The following code example shows how a WPD application initiates the command sequence.</span></span>


```C++
#include <portabledevice.h>
#include <portabledeviceapi.h>
#include <wpdmtpextensions.h>

HRESULT SetDateTime(IPortableDevice* pDevice, LPCWSTR pwszDateTime)
{
    HRESULT hr = S_OK;
    const WORD PTP_OPCODE_SETDEVICEPROPVALUE = 0x1016; 
    const WORD PTP_DEVICEPROPCODE_DATETIME = 0x5011; 
    const WORD PTP_RESPONSECODE_OK = 0x2001;     // 0x2001 indicates command success

    // Build basic WPD parameters for the command
    CComPtr<IPortableDeviceValues> spParameters;
    if (hr == S_OK)
    {
        hr = CoCreateInstance(CLSID_PortableDeviceValues,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_IPortableDeviceValues,
                              (VOID**)&spParameters);
    }

    // Use WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITH_DATA_TO_WRITE
    if (hr == S_OK)
    {
        hr = spParameters->SetGuidValue(WPD_PROPERTY_COMMON_COMMAND_CATEGORY, 
                                           WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITH_DATA_TO_WRITE.fmtid);
    }

    if (hr == S_OK)
    {
        hr = spParameters->SetUnsignedIntegerValue(WPD_PROPERTY_COMMON_COMMAND_ID, 
                                              WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITH_DATA_TO_WRITE.pid);
    }

    // Specify the actual MTP op-code to execute here
    if (hr == S_OK)
    {
        hr = spParameters->SetUnsignedIntegerValue(WPD_PROPERTY_MTP_EXT_OPERATION_CODE, 
                                                      (ULONG) PTP_OPCODE_SETDEVICEPROPVALUE);
    }

    // SetDevicePropValue requires the property code as an MTP parameter
    // MTP parameters need to be first put into a PropVariantCollection
    CComPtr<IPortableDevicePropVariantCollection> spMtpParams;
    if (hr == S_OK)
    {
        hr = CoCreateInstance(CLSID_PortableDevicePropVariantCollection,
                                  NULL,
                                  CLSCTX_INPROC_SERVER,
                                  IID_IPortableDevicePropVariantCollection,
                                  (VOID**)&spMtpParams);
    }

    PROPVARIANT pvParam = {0};
    pvParam.vt = VT_UI4;

    // Specify the DateTime property as the MTP parameter
    if (hr == S_OK)
    {
        pvParam.ulVal = PTP_DEVICEPROPCODE_DATETIME;
        hr = spMtpParams->Add(&pvParam);
    }

    // Add MTP parameters collection to our main parameter list
    if (hr == S_OK)
    {
        hr = spParameters->SetIPortableDevicePropVariantCollectionValue(
                                          WPD_PROPERTY_MTP_EXT_OPERATION_PARAMS, spMtpParams);
    }  

    // Figure out the data to send - in this case it will be an MTP string
    BYTE* pbBuffer = NULL;
    DWORD cbBufferSize = 0;
    if (hr == S_OK)
    {
        hr = PackString(pwszDateTime, &pbBuffer, &cbBufferSize);
    }

    // Inform the device how much data will arrive - this is a required parameter
    if (hr == S_OK)
    {
        hr = spParameters->SetUnsignedLargeIntegerValue(WPD_PROPERTY_MTP_EXT_TRANSFER_TOTAL_DATA_SIZE, 
                                                        &cbBufferSize);
    }

    // Send the command to initiate the transfer
    CComPtr<IPortableDeviceValues> spResults;
    if (hr == S_OK)
    {
        hr = pDevice->SendCommand(0, spParameters, &spResults);
    }

    // Check if the driver was able to send the command by interrogating WPD_PROPERTY_COMMON_HRESULT
    HRESULT hrCmd = S_OK;
    if (hr == S_OK)
    {
         hr = spResults->GetErrorValue(WPD_PROPERTY_COMMON_HRESULT, &hrCmd);
    }

    if (hr == S_OK)
    {
        printf("Driver return code (initiating): 0x%08X\n", hrCmd);
        hr = hrCmd;
    }

    // The driver returns a context cookie that we need to use during our data transfer
    LPWSTR pwszCookie = NULL;
    if (hr == S_OK)
    {
         hr = spResults->GetStringValue(WPD_PROPERTY_MTP_EXT_TRANSFER_CONTEXT, &pwszContext);
    }
```



<span data-ttu-id="0950d-120">L’exemple de code suivant montre comment une application WPD transmet les données après l’initialisation de la commande.</span><span class="sxs-lookup"><span data-stu-id="0950d-120">The following code example shows how a WPD application transmits the data after it has initiated the command.</span></span>


```
   // Use the WPD_COMMAND_MTP_EXT_WRITE_DATA command to send the data
    (void) spParameters->Clear();
    if (hr == S_OK)
    {
        hr = spParameters->SetGuidValue(WPD_PROPERTY_COMMON_COMMAND_CATEGORY, 
                                           WPD_COMMAND_MTP_EXT_WRITE_DATA.fmtid);
    }

    if (hr == S_OK)
    {
        hr = spParameters->SetUnsignedIntegerValue(WPD_PROPERTY_COMMON_COMMAND_ID, 
                                                      WPD_COMMAND_MTP_EXT_WRITE_DATA.pid);
    }

    // Specify the same context that we received earlier
    if (hr == S_OK)
    {
        hr = spParameters->SetStringValue(WPD_PROPERTY_MTP_EXT_TRANSFER_CONTEXT, pwszContext);   
    }

    // Specify the number of bytes that arrive with this command. This allows us to 
    // send the data in chunks if required (multiple WRITE_DATA commands). In this case,    //  send the data in a single chunk
    if (hr == S_OK)
    {
        hr = spParameters->SetUnsignedIntegerValue(WPD_PROPERTY_MTP_EXT_TRANSFER_NUM_BYTES_TO_WRITE, 
                                                   cbBufferSize);
    }

    // Provide the data that needs to be transferred
    if (hr == S_OK)
    {
        hr = spParameters->SetBufferValue(WPD_PROPERTY_MTP_EXT_TRANSFER_DATA, pbBuffer, cbBufferSize);
    }

    // Send the data to the device
    spResults = NULL;
    if (hr == S_OK)
    {
        hr = pDevice->SendCommand(0, spParameters, &spResults);
    }

    // Check if the data was sent successfully by interrogating COMMON_HRESULT
    if (hr == S_OK)
    {
         hr = spResults->GetErrorValue(WPD_PROPERTY_COMMON_HRESULT, &hrCmd);
    }

    if (hr == S_OK)
    {
        printf("Driver return code (sending data): 0x%08X\n", hrCmd);
        hr = hrCmd;
    }

    // The driver informs us about the number of bytes that were actually transferred. Normally this
    // should be the same as the number that we provided.
    DWORD cbBytesWritten = 0;
    if (hr == S_OK)
    {
        hr = spResults->GetUnsignedIntegerValue(WPD_PROPERTY_MTP_EXT_TRANSFER_NUM_BYTES_WRITTEN, 
                                                &cbBytesWritten);
    }
```



<span data-ttu-id="0950d-121">L’exemple de code suivant montre comment une application récupère un code de réponse de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0950d-121">The following code example shows how an application retrieves a response code from the device.</span></span>


```
   // Use the WPD_COMMAND_MTP_EXT_END_DATA_TRANSFER command to signal transfer completion
    (void) spParameters->Clear();
    if (hr == S_OK)
    {
        hr = spParameters->SetGuidValue(WPD_PROPERTY_COMMON_COMMAND_CATEGORY, 
                                           WPD_COMMAND_MTP_EXT_END_DATA_TRANSFER.fmtid);
    }

    if (hr == S_OK)
    {
        hr = spParameters->SetUnsignedIntegerValue(WPD_PROPERTY_COMMON_COMMAND_ID, 
                                                      WPD_COMMAND_MTP_EXT_END_DATA_TRANSFER.pid);
    }

    // Specify the same context that we received earlier
    if (hr == S_OK)
    {
        hr = spParameters->SetStringValue(WPD_PROPERTY_MTP_EXT_TRANSFER_CONTEXT, pwszContext);   
    }

    // Send the completion command
    spResults = NULL;
    if (hr == S_OK)
    {
        hr = pDevice->SendCommand(0, spParameters, &spResults);
    }

    // Check if the driver successfully ended the data transfer
    if (hr == S_OK)
    {
         hr = spResults->GetErrorValue(WPD_PROPERTY_COMMON_HRESULT, &hrCmd);
    }

    if (hr == S_OK)
    {
        printf("Driver return code (ending transfer): 0x%08X\n", hrCmd);
        hr = hrCmd;
    }

    // If the command was executed successfully, check the MTP response code to see if the
    // device can handle the command and the data. Be aware that there is a distinction between the command
    // and the data being successfully sent to the device and the command and data being handled successfully 
    // by the device
    DWORD dwResponseCode;
    if (hr == S_OK)
    {
        hr = spResults->GetUnsignedIntegerValue(WPD_PROPERTY_MTP_EXT_RESPONSE_CODE, &dwResponseCode);
    }

    if (hr == S_OK)
    {
        printf("MTP Response code: 0x%X\n", dwResponseCode);
        hr = (dwResponseCode == (DWORD) PTP_RESPONSECODE_OK) ? S_OK : E_FAIL;
    }

    // If response parameters are present, they will be contained in the WPD_PROPERTY_MTP_EXT_RESPONSE_PARAMS 
    // property. SetDevicePropValue does not return additional response parameters, so skip this code 
    

    // Free up any allocated memory
    CoTaskMemFree(pbBuffer);
    CoTaskMemFree(pwszContext);

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="0950d-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0950d-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0950d-123">Prise en charge des extensions MTP</span><span class="sxs-lookup"><span data-stu-id="0950d-123">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 



