---
title: IVMSerialPort configure, méthode (VPCCOMInterfaces. h)
description: Configure le port série.
ms.assetid: fee2e373-8e7c-4f1d-84d0-f0f187a41e9f
keywords:
- Configurer la méthode Virtual PC
- Configurer la méthode Virtual PC, interface IVMSerialPort
- IVMSerialPort interface Virtual PC, configurer la méthode
topic_type:
- apiref
api_name:
- IVMSerialPort.Configure
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c99440263dbf52282b6f3c2756ff7dd76151ff73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032930"
---
# <a name="ivmserialportconfigure-method"></a><span data-ttu-id="b6087-106">IVMSerialPort :: configure, méthode</span><span class="sxs-lookup"><span data-stu-id="b6087-106">IVMSerialPort::Configure method</span></span>

<span data-ttu-id="b6087-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b6087-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b6087-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b6087-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b6087-109">Configure le port série.</span><span class="sxs-lookup"><span data-stu-id="b6087-109">Configures the serial port.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6087-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b6087-110">Syntax</span></span>


```C++
HRESULT Configure(
  [in] VMSerialPortType portType,
  [in] BSTR             portName,
  [in] VARIANT_BOOL     vmConnectImmediately
);
```



## <a name="parameters"></a><span data-ttu-id="b6087-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b6087-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6087-112">*portType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b6087-112">*portType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6087-113">Type de port série.</span><span class="sxs-lookup"><span data-stu-id="b6087-113">The type of serial port.</span></span> <span data-ttu-id="b6087-114">Pour obtenir la liste des valeurs, consultez [**VMSerialPortType**](vmserialporttype.md).</span><span class="sxs-lookup"><span data-stu-id="b6087-114">For a list of values, see [**VMSerialPortType**](vmserialporttype.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6087-115">*PortName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b6087-115">*portName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6087-116">Nom du port série.</span><span class="sxs-lookup"><span data-stu-id="b6087-116">The name of the serial port.</span></span> <span data-ttu-id="b6087-117">Par exemple, « COM1 » pour **vmSerialPort \_ appelait hostport**, « C : \\SerialPort.txt » pour **vmSerialPort \_ TextFile**, ou « \\ \\ *ServerName* \\ pipe \\ *pipeName*» pour **vmSerialPort \_ NamedPipe**.</span><span class="sxs-lookup"><span data-stu-id="b6087-117">For example, "COM1" for **vmSerialPort\_HostPort**, "C:\\SerialPort.txt" for **vmSerialPort\_TextFile**, or "\\\\*servername*\\pipe\\*pipename*" for **vmSerialPort\_NamedPipe**.</span></span>

</dd> <dt>

<span data-ttu-id="b6087-118">*vmConnectImmediately* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b6087-118">*vmConnectImmediately* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6087-119">**True** si le port série de l’hôte doit être ouvert immédiatement au démarrage de l’ordinateur virtuel et **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="b6087-119">**TRUE** if the host serial port should be opened immediately when the virtual machine is started and **FALSE** otherwise.</span></span> <span data-ttu-id="b6087-120">Ignoré si *portType* n’est pas **vmSerialPort \_ appelait hostport**.</span><span class="sxs-lookup"><span data-stu-id="b6087-120">Ignored if *portType* is not **vmSerialPort\_HostPort**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6087-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b6087-121">Return value</span></span>

<span data-ttu-id="b6087-122">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="b6087-122">This method can return one of these values.</span></span>



| <span data-ttu-id="b6087-123">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="b6087-123">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="b6087-124">Description</span><span class="sxs-lookup"><span data-stu-id="b6087-124">Description</span></span>                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b6087-125"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b6087-125"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="b6087-126">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="b6087-126">The operation was successful.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="b6087-127"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="b6087-127"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                 | <span data-ttu-id="b6087-128">Le paramètre *portType* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="b6087-128">The *portType* parameter is not valid.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="b6087-129"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="b6087-129"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="b6087-130">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="b6087-130">An unexpected error has occurred.</span></span><br/>                                                                                      |
| <dl> <span data-ttu-id="b6087-131"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="b6087-131"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="b6087-132">Le paramètre *PortName* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="b6087-132">The *portName* parameter is **NULL**.</span></span><br/>                                                                                  |
| <dl> <span data-ttu-id="b6087-133">Valeur <dt>**HRESULT \_ À partir de \_ Win32 (erreur \_ OUTOFMEMORY)**</dt> <dt>0x8007000E</dt></span><span class="sxs-lookup"><span data-stu-id="b6087-133"><dt>**HRESULT\_FROM\_WIN32(ERROR\_OUTOFMEMORY)**</dt> <dt>0x8007000e</dt></span></span> </dl>      | <span data-ttu-id="b6087-134">La mémoire disponible est insuffisante pour effectuer cette requête.</span><span class="sxs-lookup"><span data-stu-id="b6087-134">There is not enough memory available to complete this request.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="b6087-135">Valeur <dt>**HRESULT \_ À partir de \_ Win32 \_ ( \_ dépassement de mémoire tampon d’erreur)**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="b6087-135"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="b6087-136">Le chemin d’accès spécifié par le paramètre *PortName* est trop long.</span><span class="sxs-lookup"><span data-stu-id="b6087-136">The path specified by the *portName* parameter is too long.</span></span> <span data-ttu-id="b6087-137">Le chemin d’accès doit être inférieur à la **longueur maximale \_** (260) caractères.</span><span class="sxs-lookup"><span data-stu-id="b6087-137">The path must be less than **MAX\_PATH** (260) characters.</span></span><br/> |
| <dl> <span data-ttu-id="b6087-138">Valeur <dt>**HRESULT \_ À partir de \_ Win32 (erreur \_ \_ nom non valide)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="b6087-138"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="b6087-139">Le paramètre *PortName* contient un caractère non valide (l’un des caractères \* suivants : «  ? <>/ \| » :»).</span><span class="sxs-lookup"><span data-stu-id="b6087-139">The *portName* parameter contains an invalid character (one of "\*?<>/\|":").</span></span><br/>                                    |
| <dl> <span data-ttu-id="b6087-140">Valeur <dt>**HRESULT \_ FROM \_ Win32 (erreur \_ de \_ nom de chemin incorrect)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="b6087-140"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="b6087-141">Le paramètre *PortName* spécifie un chemin d’accès vide ou relatif.</span><span class="sxs-lookup"><span data-stu-id="b6087-141">The *portName* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="b6087-142">Un chemin d’accès absolu est requis.</span><span class="sxs-lookup"><span data-stu-id="b6087-142">An absolute path is required.</span></span><br/>                            |
| <dl> <span data-ttu-id="b6087-143"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="b6087-143"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                            | <span data-ttu-id="b6087-144">La configuration de cet ordinateur virtuel n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="b6087-144">The configuration for this virtual machine is not valid.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="b6087-145"><dt>**Ordinateur virtuel \_ E \_ pref \_ \_ valeur non conforme**</dt> <dt>0xA0040301</dt></span><span class="sxs-lookup"><span data-stu-id="b6087-145"><dt>**VM\_E\_PREF\_ILLEGAL\_VALUE**</dt> <dt>0xA0040301</dt></span></span> </dl>                   | <span data-ttu-id="b6087-146">Le port spécifié est déjà utilisé.</span><span class="sxs-lookup"><span data-stu-id="b6087-146">The specified port is already in use.</span></span><br/>                                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="b6087-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b6087-147">Requirements</span></span>



| <span data-ttu-id="b6087-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b6087-148">Requirement</span></span> | <span data-ttu-id="b6087-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="b6087-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6087-150">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b6087-150">Minimum supported client</span></span><br/> | <span data-ttu-id="b6087-151">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b6087-151">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b6087-152">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b6087-152">Minimum supported server</span></span><br/> | <span data-ttu-id="b6087-153">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b6087-153">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b6087-154">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="b6087-154">End of client support</span></span><br/>    | <span data-ttu-id="b6087-155">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b6087-155">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b6087-156">Produit</span><span class="sxs-lookup"><span data-stu-id="b6087-156">Product</span></span><br/>                  | <span data-ttu-id="b6087-157">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b6087-157">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b6087-158">En-tête</span><span class="sxs-lookup"><span data-stu-id="b6087-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6087-159"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6087-159"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b6087-160">IID</span><span class="sxs-lookup"><span data-stu-id="b6087-160">IID</span></span><br/>                      | <span data-ttu-id="b6087-161">IID \_ IVMSerialPort est défini en tant que 2ce4460d-1d3f-4458-BF8B-44084b816815</span><span class="sxs-lookup"><span data-stu-id="b6087-161">IID\_IVMSerialPort is defined as 2ce4460d-1d3f-4458-bf8b-44084b816815</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="b6087-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6087-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6087-163">**IVMSerialPort**</span><span class="sxs-lookup"><span data-stu-id="b6087-163">**IVMSerialPort**</span></span>](ivmserialport.md)
</dt> </dl>

 

